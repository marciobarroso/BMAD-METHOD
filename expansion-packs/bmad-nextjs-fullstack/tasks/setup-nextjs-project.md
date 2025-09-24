# Setup Next.js Project

## Task Overview

Initialize a new Next.js project with TypeScript, Tailwind CSS, ESLint, and Prettier configuration.

## Prerequisites

- Node.js 18+ installed
- npm or yarn package manager
- Git for version control

## Steps

### 1. Create Next.js Project

```bash
npx create-next-app@latest {project_name} --typescript --tailwind --eslint --app --src-dir --import-alias "@/*"
cd {project_name}
```

### 2. Install Additional Dependencies

```bash
npm install --save-dev prettier prettier-plugin-tailwindcss @types/node
npm install lucide-react clsx tailwind-merge
```

### 3. Configure Prettier

Create `.prettierrc.json`:

```json
{
  "semi": false,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "es5",
  "printWidth": 80,
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

### 4. Update ESLint Configuration

Extend `.eslintrc.json`:

```json
{
  "extends": ["next/core-web-vitals", "prettier"],
  "rules": {
    "prefer-const": "error",
    "no-unused-vars": "error"
  }
}
```

### 5. Configure TypeScript

Update `tsconfig.json` for strict mode:

```json
{
  "compilerOptions": {
    "strict": true,
    "noUnusedLocals": true,
    "noUnusedParameters": true,
    "exactOptionalPropertyTypes": true
  }
}
```

### 6. Set up Scripts

Add to `package.json`:

```json
{
  "scripts": {
    "format": "prettier --write .",
    "format:check": "prettier --check .",
    "lint:fix": "eslint . --fix"
  }
}
```

## Validation Checklist

- [ ] Next.js project created with TypeScript
- [ ] Tailwind CSS configured and working
- [ ] ESLint and Prettier configured
- [ ] All dependencies installed
- [ ] Scripts working correctly
- [ ] Project builds without errors

## Next Steps

- Set up folder structure
- Configure environment variables
- Create initial components
