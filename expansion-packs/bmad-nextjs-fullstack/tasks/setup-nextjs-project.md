# Setup Next.js Project from Template

## Task Overview

Initialize a new Feature-Based Architecture project using the pre-configured `nextjs-new-app` template with Next.js 15+, TypeScript, Tailwind CSS 4.x, and development tooling.

## Prerequisites

- Node.js 20.10.0+ installed
- pnpm (recommended) or npm package manager
- Git for version control
- Access to https://github.com/marciobarroso/nextjs-new-app

## Steps

### 1. Clone Template Repository

```bash
# Clone the nextjs-new-app template
git clone https://github.com/marciobarroso/nextjs-new-app.git {project_name}
cd {project_name}

# Remove original git history and initialize new repository
rm -rf .git
git init
git add .
git commit -m "Initial commit from nextjs-new-app template"
```

### 2. Install Dependencies

```bash
# Install using pnpm (recommended by template)
pnpm install

# Alternative: using npm
# npm install
```

### 3. Configure Project Details

Update `package.json`:

```json
{
  "name": "{project_name}",
  "version": "1.0.0",
  "description": "{project_description}",
  "author": "{author_name}"
}
```

### 4. Set Up Feature-Based Architecture Structure

```bash
# Create the Feature-Based Architecture directories
mkdir -p app/\(features\)
mkdir -p app/shared/core
mkdir -p app/shared/types
mkdir -p app/shared/lib

# The template already provides:
# - app/shared/components/
# - app/shared/hooks/
# - app/shared/lib/
# - app/shared/locales/
```

### 5. Implement BaseController Foundation

Create `app/shared/core/base-controller.ts`:

```typescript
import { z } from 'zod';
import { NextRequest, NextResponse } from 'next/server';

export abstract class BaseController<T> {
  protected dbClient: any;
  protected schema?: z.ZodSchema;

  constructor(dbClient: any, schema?: z.ZodSchema) {
    this.dbClient = dbClient;
    this.schema = schema;
  }

  // Standard CRUD operations
  async getAll(request: NextRequest): Promise<NextResponse> {
    try {
      const { searchParams } = new URL(request.url);
      const query = searchParams.get('query');
      const page = parseInt(searchParams.get('page') || '1');
      const limit = parseInt(searchParams.get('limit') || '20');

      const filter = this.buildSearchFilter(query);
      // Implement database-specific query here

      return NextResponse.json({
        data: [],
        pagination: { page, limit, total: 0, totalPages: 0 },
        success: true,
      });
    } catch (error) {
      return NextResponse.json(
        { error: 'Failed to fetch records', success: false },
        { status: 500 },
      );
    }
  }

  async getById(
    request: NextRequest,
    { params }: { params: { id: string } },
  ): Promise<NextResponse> {
    try {
      // Implement database-specific findById here
      return NextResponse.json({ data: null, success: true });
    } catch (error) {
      return NextResponse.json(
        { error: 'Failed to fetch record', success: false },
        { status: 500 },
      );
    }
  }

  async create(request: NextRequest): Promise<NextResponse> {
    try {
      const body = await request.json();

      if (this.schema) {
        const validatedData = this.schema.parse(body);
        // Implement database-specific create here
      }

      return NextResponse.json({ data: null, success: true }, { status: 201 });
    } catch (error) {
      if (error instanceof z.ZodError) {
        return NextResponse.json(
          { error: 'Validation failed', details: error.errors, success: false },
          { status: 400 },
        );
      }
      return NextResponse.json(
        { error: 'Failed to create record', success: false },
        { status: 500 },
      );
    }
  }

  async update(
    request: NextRequest,
    { params }: { params: { id: string } },
  ): Promise<NextResponse> {
    try {
      const body = await request.json();

      if (this.schema) {
        const validatedData = this.schema.partial().parse(body);
        // Implement database-specific update here
      }

      return NextResponse.json({ data: null, success: true });
    } catch (error) {
      if (error instanceof z.ZodError) {
        return NextResponse.json(
          { error: 'Validation failed', details: error.errors, success: false },
          { status: 400 },
        );
      }
      return NextResponse.json(
        { error: 'Failed to update record', success: false },
        { status: 500 },
      );
    }
  }

  async delete(
    request: NextRequest,
    { params }: { params: { id: string } },
  ): Promise<NextResponse> {
    try {
      // Implement database-specific delete here
      return NextResponse.json({ success: true, message: 'Record deleted successfully' });
    } catch (error) {
      return NextResponse.json(
        { error: 'Failed to delete record', success: false },
        { status: 500 },
      );
    }
  }

  // Abstract method for search filtering
  protected abstract buildSearchFilter(query: string | null): Record<string, any>;
}
```

### 6. Add Zod for Schema Validation

```bash
# Install Zod for schema validation
pnpm add zod
# or npm install zod
```

### 7. Configure Environment Variables

Create `.env.local`:

```env
# Database Configuration (customize based on your choice)
DATABASE_URL="your-database-url"

# Next.js Configuration
NEXT_PUBLIC_APP_NAME="{project_name}"
NEXT_PUBLIC_APP_VERSION="1.0.0"

# Add other environment variables as needed
```

### 8. Update TypeScript Configuration

The template already provides optimal TypeScript configuration, but you can extend `tsconfig.json` if needed:

```json
{
  "compilerOptions": {
    // Template already includes optimal settings
    "baseUrl": ".",
    "paths": {
      "@/*": ["./*"]
    }
  }
}
```

### 9. Test the Setup

```bash
# Run development server
pnpm dev
# or npm run dev

# Run linting
pnpm lint
# or npm run lint

# Run formatting
pnpm format
# or npm run format

# Run build test
pnpm build
# or npm run build
```

### 10. Initialize Git Repository

```bash
# Add remote repository (replace with your repository URL)
git remote add origin https://github.com/yourusername/{project_name}.git

# Make initial commit with template
git add .
git commit -m "feat: initialize project from nextjs-new-app template

- Set up Next.js 15+ with TypeScript and Tailwind CSS 4.x
- Implemented Feature-Based Architecture structure
- Added BaseController foundation for database-agnostic patterns
- Configured development tooling (ESLint, Prettier, Husky)

Template: https://github.com/marciobarroso/nextjs-new-app"

# Push to remote repository
git push -u origin main
```

## Validation Checklist

- [ ] Template repository successfully cloned
- [ ] Dependencies installed without errors
- [ ] Development server runs on http://localhost:3000
- [ ] ESLint and Prettier configured and working
- [ ] TypeScript compilation successful
- [ ] Feature-Based Architecture directories created
- [ ] BaseController foundation implemented
- [ ] Zod schema validation set up
- [ ] Environment variables configured
- [ ] Git repository initialized and connected

## Template Features Already Configured

- ✅ Next.js 15.5.3 with App Router
- ✅ React 19.1.0 with latest features
- ✅ TypeScript 5 with strict configuration
- ✅ Tailwind CSS 4.1.13 with PostCSS
- ✅ ESLint 9 with Next.js integration
- ✅ Prettier 3.6.2 with import sorting
- ✅ Husky 9.1.7 for git hooks
- ✅ Jest testing framework (configured)
- ✅ Shared components structure
- ✅ Basic layouts and providers
- ✅ Internationalization setup

## Next Steps After Setup

1. Plan your first business domain feature
2. Implement your chosen database integration (Prisma, TypeORM, Mongoose, etc.)
3. Create your first feature following Feature-Based Architecture
4. Set up authentication system
5. Configure your preferred database
6. Implement testing for your features
7. Set up CI/CD pipeline for deployment

## Database Integration Examples

### For Prisma (PostgreSQL)

```bash
pnpm add prisma @prisma/client
pnpm add -D prisma
npx prisma init
```

### For TypeORM (SQL databases)

```bash
pnpm add typeorm reflect-metadata
pnpm add pg # for PostgreSQL
# or pnpm add mysql2 # for MySQL
```

### For Mongoose (MongoDB)

```bash
pnpm add mongoose
pnpm add -D @types/mongoose
```

The `nextjs-new-app` template provides an excellent foundation for Feature-Based Architecture, and this setup process will get you ready to build scalable, maintainable Next.js applications following Domain-Driven Design principles.
