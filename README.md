# mstrymessage

mstrymessage is an anonymous messaging platform built with Next.js. Users can sign up, verify their account via an email code, and receive anonymous messages on their dashboard.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Technology Stack](#technology-stack)
- [Available Scripts](#available-scripts)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication:** Sign up, sign in, and account verification using OTP.
- **Anonymous Messaging:** Send and receive anonymous messages.
- **User Dashboard:** Manage and view messages.
- **Live Updates:** Refresh messages and toggle acceptance of new messages.
- **Responsive Design:** Clean UI built with Tailwind CSS.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en/) (v14 or later)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd mstrymessage
   ```
2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```
3. Create a `.env.local` file at the project root with the following variables (adjust as needed):
   ```
   NEXTAUTH_SECRET=<your-next-auth-secret>
   DATABASE_URL=<your-database-connection-string>
   EMAIL_SERVER=<your-email-server-configurations>
   EMAIL_FROM=<your-email-from-address>
   ```
4. Run the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```
5. Open [http://localhost:3000](http://localhost:3000) with your browser.

## Project Structure

```plaintext
mstrymessage/
├── app/                 # Next.js app directory (layout, pages, etc.)
├── components/          # UI and functional components (Navbar, MessageCard, etc.)
├── emails/              # Email templates (e.g., VerificationEmail.tsx)
├── public/              # Static assets
├── schemas/             # Zod schemas for form validation
├── context/             # React context providers (e.g., AuthProvider)
├── messages.json        # Sample messages data
├── package.json         # Project metadata and scripts
└── README.md            # Project documentation
```

## Technology Stack

- **Frontend:** Next.js, React, TypeScript, Tailwind CSS
- **Backend:** Next.js API routes, Node.js
- **Authentication:** NextAuth.js
- **Form Validation:** react-hook-form and Zod
- **Database:** MongoDB (via Mongoose) or any supported database
- **Email Verification:** @react-email/components for templating emails

## Available Scripts

Inside the project directory, you can run:

- `npm run dev`  
  Starts the Next.js development server.

- `npm run build`  
  Builds the application for production.

- `npm run start`  
  Runs the built production application.

- `npm run lint`  
  Runs ESLint to check for code quality issues.

## Deployment

mstrymessage can be deployed on platforms like Vercel. For deployment:

1. Connect your repository to [Vercel](https://vercel.com/).
2. Set environment variables in Vercel using your `.env.local` configurations.
3. Deploy the app following Vercel's deployment guidelines.

For more details on deployment, refer to the [Next.js Deployment Docs](https://nextjs.org/docs/deployment).

## Contributing

Contributions are welcome! Follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes.
4. Push to the branch.
5. Open a Pull Request.

Please adhere to code style and testing guidelines.

## License

This project is [MIT licensed](LICENSE).
