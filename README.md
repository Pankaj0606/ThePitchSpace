# ThePitchSpace Documentation
## Project Overview
ThePitchSpace is a platform designed to connect startups with entrepreneurs, allowing them to pitch their ideas, vote on other pitches, and gain visibility. It aims to foster a community where innovative ideas can be shared and evaluated.
**Key Features:**
*   **Startup Pitching:** Users can submit their startup ideas with detailed descriptions and supporting information.
*   **Voting System:** Community members can vote on startup pitches, providing feedback and highlighting promising ideas.
*   **Search Functionality:** Users can search for startups based on keywords, categories, or author.
*   **User Profiles:** Each user has a profile page showcasing their submitted startups and personal information.
*   **Editor Picks:** Curated selection of startups highlighted by the platform's editors.
*   **Sanity Studio Integration:** A built-in authoring environment for content management using Sanity Studio.
*   **Sentry Integration:** Error monitoring and performance tracking using Sentry.
**Supported Platforms/Requirements:**
*   Next.js
*   Node.js
*   Sanity.io
*   GitHub Authentication
## Getting Started
### Installation
1.  **Clone the repository:**
    ```bash
    git clone <repository_url>
    cd yc_directory
    ```
    
2.  **Install dependencies:**
    ```bash
    npm install
    ```
    
3.  **Set up environment variables:**
    *   Create a `.env` file in the root directory.
    *   Add the following environment variables, replacing the placeholders with your actual values:
                NEXT_PUBLIC_SANITY_PROJECT_ID=<your_sanity_project_id>
        NEXT_PUBLIC_SANITY_DATASET=<your_sanity_dataset>
        NEXT_PUBLIC_SANITY_API_VERSION="2024-10-14"
        SANITY_WRITE_TOKEN=<your_sanity_write_token>
        GITHUB_ID=<your_github_app_id>
        GITHUB_SECRET=<your_github_app_secret>
        NEXTAUTH_SECRET=<a_secure_random_string>
        NEXTAUTH_URL=http://localhost:3000 # or your deployed URL
        SENTRY_DSN=<your_sentry_dsn>
        
4.  **Configure Sanity:**
    *   Install the Sanity CLI globally:
        ```bash
        npm install -g @sanity/cli
        ```
        
    *   Log in to your Sanity account:
        ```bash
        sanity login
        ```
        
    *   Deploy the Sanity schema:
        ```bash
        sanity deploy
        ```
        
5.  **Run the development server:**
    ```bash
    npm run dev
    ```
    
    The application should now be running at `http://localhost:3000`.
### Dependencies
*   **Next.js:** A React framework for building web applications.
*   **React:** A JavaScript library for building user interfaces.
*   **Sanity.io:** A headless CMS for managing content.
*   **next-auth:** Authentication library for Next.js.
*   **@radix-ui/react-\*:** Set of accessible UI primitives.
*   **class-variance-authority:** Utility for composing variant-aware class names.
*   **clsx:** Utility for conditionally joining class names.
*   **tailwind-merge:** Utility for merging Tailwind CSS classes.
*   **tailwindcss:** CSS framework.
*   **lucide-react:** Icon library.
*   **@uiw/react-md-editor:** Markdown editor component.
*   **slugify:** Utility for creating slugs from strings.
*   **@sentry/nextjs:** Sentry integration for Next.js.
*   **markdown-it:** Markdown parser.

**Key Components:**
*   **`app/`:** Contains the Next.js application routes and pages.
*   **`components/`:** Houses reusable UI components.
*   **`lib/`:** Contains utility functions, server actions, and validation schemas.
*   **`sanity/`:** Contains Sanity CMS configuration, schemas, and data fetching logic.
*   **`auth.ts`:** Configures authentication using NextAuth.
*   **`next.config.ts`:** Configures the Next.js application.
*   **`tailwind.config.ts`:** Configures Tailwind CSS.
## API Documentation
### Endpoints
#### `GET /api/sentry-example-api`
*   **Purpose:** A faulty API route to test Sentry's error monitoring.
*   **Description:** This endpoint intentionally throws an error to trigger Sentry's error tracking.
*   **Input:** None
*   **Output:**
    *   Throws an error: `"Sentry Example API Route Error"`
    ```json
    {
      "data": "Testing Sentry Error..."
    }
    
    ```
