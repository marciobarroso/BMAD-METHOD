# Create API Endpoint

## Task Overview

Create a new API endpoint in Next.js with proper TypeScript typing, validation, and error handling.

## Prerequisites

- Next.js project with App Router
- TypeScript configured
- Understanding of HTTP methods and status codes

## Steps

### 1. Create API Route File

Create `src/app/api/{endpoint}/route.ts`:

```typescript
import { NextRequest, NextResponse } from 'next/server';

// Define request/response types
interface RequestBody {
  // Define your request body structure
}

interface ResponseData {
  // Define your response structure
}

export async function GET(request: NextRequest) {
  try {
    // Handle GET request logic
    const data: ResponseData = {
      // Your response data
    };

    return NextResponse.json(data, { status: 200 });
  } catch (error) {
    console.error('API Error:', error);
    return NextResponse.json({ error: 'Internal server error' }, { status: 500 });
  }
}

export async function POST(request: NextRequest) {
  try {
    const body: RequestBody = await request.json();

    // Validate request body
    if (!body) {
      return NextResponse.json({ error: 'Request body is required' }, { status: 400 });
    }

    // Handle POST request logic
    const data: ResponseData = {
      // Your response data
    };

    return NextResponse.json(data, { status: 201 });
  } catch (error) {
    console.error('API Error:', error);
    return NextResponse.json({ error: 'Internal server error' }, { status: 500 });
  }
}
```

### 2. Add Request Validation (Optional)

Install and use Zod for validation:

```bash
npm install zod
```

```typescript
import { z } from 'zod';

const requestSchema = z.object({
  name: z.string().min(1),
  email: z.string().email(),
});

export async function POST(request: NextRequest) {
  try {
    const body = await request.json();
    const validatedData = requestSchema.parse(body);

    // Use validatedData safely
  } catch (error) {
    if (error instanceof z.ZodError) {
      return NextResponse.json(
        { error: 'Invalid request data', details: error.errors },
        { status: 400 },
      );
    }
    // Handle other errors
  }
}
```

### 3. Create API Client Helper

Create `src/lib/api-client.ts`:

```typescript
class ApiError extends Error {
  constructor(
    public status: number,
    message: string,
  ) {
    super(message);
    this.name = 'ApiError';
  }
}

export async function apiCall<T>(url: string, options?: RequestInit): Promise<T> {
  const response = await fetch(url, {
    headers: {
      'Content-Type': 'application/json',
      ...options?.headers,
    },
    ...options,
  });

  if (!response.ok) {
    throw new ApiError(response.status, `HTTP error! status: ${response.status}`);
  }

  return response.json();
}
```

### 4. Use in Components

```typescript
'use client'

import { useState } from 'react'
import { apiCall } from '@/lib/api-client'

export function ExampleComponent() {
  const [loading, setLoading] = useState(false)
  const [data, setData] = useState(null)

  const handleSubmit = async () => {
    setLoading(true)
    try {
      const result = await apiCall('/api/example', {
        method: 'POST',
        body: JSON.stringify({ /* your data */ }),
      })
      setData(result)
    } catch (error) {
      console.error('Error:', error)
    } finally {
      setLoading(false)
    }
  }

  return (
    // Your component JSX
  )
}
```

## Validation Checklist

- [ ] API route file created in correct location
- [ ] Proper TypeScript types defined
- [ ] Error handling implemented
- [ ] Request validation added (if needed)
- [ ] API tested with different HTTP methods
- [ ] Client-side integration working
- [ ] Error cases handled gracefully

## Best Practices

- Use proper HTTP status codes
- Implement consistent error response format
- Add request validation for security
- Log errors for debugging
- Consider rate limiting for production
- Document API endpoints
