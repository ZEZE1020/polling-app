# Polling App

A modern polling application built with Next.js, Supabase, and shadcn/ui that allows users to create polls, vote, and view results.

## Project Overview

This application provides a platform for creating and participating in polls. Users can register, log in, create polls, vote on existing polls, and view poll results in real-time.

### Features

- **User Authentication**: Register and login functionality using Supabase Auth
- **Poll Creation**: Create polls with multiple options
- **Voting**: Vote on polls with real-time updates
- **Results Visualization**: View poll results with visual representations
- **Responsive Design**: Works on desktop and mobile devices

## Project Structure

```
polling-app/
├── app/                    # Next.js app directory
│   ├── api/                # API routes
│   ├── auth/               # Authentication pages
│   │   ├── login/          # Login page
│   │   └── register/       # Registration page
│   └── layout.tsx          # Root layout with HTML structure
├── components/             # React components
│   ├── LoginForm.tsx       # Login form component
│   └── RegisterForm.tsx    # Registration form component
├── contexts/               # React contexts
│   └── AuthContext.tsx     # Authentication context
├── lib/                    # Utility libraries
│   └── supabaseClient.ts   # Supabase client configuration
├── public/                 # Static assets
└── src/                    # Source directory
    ├── app/                # Next.js app directory (alternative)
    │   ├── globals.css     # Global CSS
    │   └── page.tsx        # Home page
    ├── components/         # UI components
    │   └── ui/             # shadcn/ui components
    └── lib/                # Utility functions
        └── utils.ts        # Helper utilities
```

## Technologies Used

- **Frontend**: Next.js, React, TypeScript, Tailwind CSS
- **UI Components**: shadcn/ui
- **Backend**: Supabase (Authentication, Database)
- **Form Handling**: react-hook-form, zod
- **Styling**: Tailwind CSS

## Getting Started

### Prerequisites

- Node.js 18.x or later
- npm or yarn
- Supabase account

### Supabase Setup

1. Create a new project on [Supabase](https://supabase.com)
2. Set up authentication:
   - Go to Authentication > Settings
   - Enable Email provider
   - Configure any additional providers as needed
3. Create necessary database tables:
   - Users table (created automatically by Supabase Auth)
   - Polls table
   - Options table
   - Votes table
4. Get your Supabase URL and anon key from the project settings

### Environment Setup

1. Clone the repository
2. Create a `.env.local` file in the root directory with the following variables:

```
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
```

### Installation

```bash
# Install dependencies
npm install
# or
yarn install

# Run the development server
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the application.

## Development Workflow

1. Authentication pages are located in `app/auth/`
2. Components are in the `components/` directory
3. Supabase client is configured in `lib/supabaseClient.ts`
4. Authentication context is in `contexts/AuthContext.tsx`

## Learn More

To learn more about the technologies used:

- [Next.js Documentation](https://nextjs.org/docs)
- [Supabase Documentation](https://supabase.com/docs)
- [shadcn/ui Documentation](https://ui.shadcn.com)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## Deployment

The application can be deployed on Vercel or any other platform that supports Next.js applications.

```bash
# Build for production
npm run build
# or
yarn build
```
