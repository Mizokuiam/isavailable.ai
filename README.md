<div align="center">
  <!-- This image is referenced locally but excluded from git via .gitignore to prevent public access -->
  <img src="github-readme.png" alt="isavailable.ai" width="100%">
  <h1>isavailable.ai</h1>
  <p>Find the perfect name for your brand. Check availability across domains, social media, and more - all in one place.</p>
  <a href="https://isavailable.ai">Visit isavailable.ai</a> | 
  <a href="https://github.com/Mizokuiam/isavailable.ai">GitHub</a> | 
  <a href="https://isavailable.ai/docs">Documentation</a>
  
  ![License](https://img.shields.io/github/license/Mizokuiam/isavailable.ai)
  ![Stars](https://img.shields.io/github/stars/Mizokuiam/isavailable.ai)
  ![Forks](https://img.shields.io/github/forks/Mizokuiam/isavailable.ai)
  ![Issues](https://img.shields.io/github/issues/Mizokuiam/isavailable.ai)
</div>

---

## 📋 Table of Contents

1. [Introduction](#1-introduction)
2. [Features](#2-features)
3. [Tech Stack](#3-tech-stack)
4. [Getting Started](#4-getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
   - [Environment Variables](#environment-variables)
   - [Running Locally](#running-locally)
5. [Architecture](#5-architecture)
6. [API Documentation](#6-api-documentation)
7. [Deployment](#7-deployment)
8. [Contributing](#8-contributing)
9. [Roadmap](#9-roadmap)
10. [License](#10-license)
11. [Acknowledgements](#11-acknowledgements)
12. [Contact](#12-contact)

---

## 1. Introduction

**isavailable.ai** is a powerful tool designed to help entrepreneurs, developers, and marketers find the perfect name for their brand or project. With a single search, you can check name availability across multiple domain extensions and social media platforms simultaneously.

Born out of the frustration of manually checking dozens of sites when launching a new project, isavailable.ai streamlines this process into seconds, saving you valuable time and helping you secure your digital identity across the web.

Our mission is to simplify the brand naming process and help creators establish a consistent online presence from day one.

---

## 2. Features

- **Comprehensive Availability Checking**
  - ✅ 30+ domain extensions (.com, .net, .org, .io, etc.)
  - ✅ 15+ social media platforms (Twitter, Instagram, GitHub, etc.)
  - ✅ Real-time verification with multiple methods

- **Advanced Search Capabilities**
  - ✅ Instant results with high accuracy
  - ✅ Filter by domains, social media, or available options
  - ✅ Detailed availability status for each platform

- **User Experience**
  - ✅ Clean, intuitive interface
  - ✅ Responsive design for all devices
  - ✅ Interactive particle network background
  - ✅ Command menu (⌘K) for quick navigation

- **Performance & Reliability**
  - ✅ Optimized API with rate limiting
  - ✅ Result caching for improved performance
  - ✅ Multiple verification methods for accuracy
  - ✅ Graceful error handling

---

## 3. Tech Stack

isavailable.ai is built with modern technologies focused on performance, scalability, and developer experience:

- **Frontend**:
  - [Next.js 14](https://nextjs.org/) - React framework with App Router
  - [TypeScript](https://www.typescriptlang.org/) - Type-safe JavaScript
  - [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
  - [Framer Motion](https://www.framer.com/motion/) - Animation library
  - [shadcn/ui](https://ui.shadcn.com/) - UI component system

- **Backend**:
  - [Next.js API Routes](https://nextjs.org/docs/api-routes/introduction) - Serverless functions
  - [Node.js](https://nodejs.org/) - JavaScript runtime

- **Infrastructure**:
  - [Vercel](https://vercel.com/) - Deployment and hosting
  - [GitHub Actions](https://github.com/features/actions) - CI/CD

---

## 4. Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v18.17.0 or higher)
- [npm](https://www.npmjs.com/) (v9.0.0 or higher) or [yarn](https://yarnpkg.com/) (v1.22.0 or higher)
- [Git](https://git-scm.com/)

### Installation

\`\`\`bash
# Clone the repository
git clone https://github.com/Mizokuiam/isavailable.ai.git

# Navigate to the project directory
cd isavailable.ai

# Install dependencies
npm install
# or
yarn install
\`\`\`

### Environment Variables

Create a `.env.local` file in the root directory with the following variables:

\`\`\`
# Base URL
NEXT_PUBLIC_BASE_URL=http://localhost:3000

# API Rate Limiting
RATE_LIMIT_REQUESTS=20
RATE_LIMIT_INTERVAL=60000

# Optional: Analytics
NEXT_PUBLIC_ANALYTICS_ID=your-analytics-id
\`\`\`

### Running Locally

\`\`\`bash
# Start the development server
npm run dev
# or
yarn dev

# Build for production
npm run build
# or
yarn build

# Start the production server
npm start
# or
yarn start
\`\`\`

The application will be available at `http://localhost:3000`.

---

## 5. Architecture

isavailable.ai follows a modern architecture pattern:

\`\`\`
┌─────────────────────────────────┐
│           Client Side           │
│  (Next.js App Router, React)    │
└───────────────┬─────────────────┘
                │
                ▼
┌─────────────────────────────────┐
│         Server Components       │
│     (Next.js, TypeScript)       │
└───────────────┬─────────────────┘
                │
                ▼
┌─────────────────────────────────┐
│           API Routes            │
│    (Next.js API, TypeScript)    │
└───────────────┬─────────────────┘
                │
                ▼
┌─────────────────────────────────┐
│       External Services         │
│  (DNS, WHOIS, Platform APIs)    │
└─────────────────────────────────┘
\`\`\`

Key architectural decisions:
- **Server Components**: Leveraging Next.js App Router for improved performance and SEO
- **API-First Design**: Clean separation between frontend and backend
- **Progressive Enhancement**: Core functionality works without JavaScript
- **Responsive Design**: Mobile-first approach for all screen sizes
- **Accessibility**: WCAG 2.1 AA compliance throughout the application

---

## 6. API Documentation

isavailable.ai offers a RESTful API for developers who want to integrate our availability checking into their own applications.

### Base URL
\`\`\`
https://isavailable.ai/api/v1
\`\`\`

### Authentication
API requests require an API key. You can obtain one by signing up for a Pro or Business plan.

\`\`\`
Authorization: Bearer YOUR_API_KEY
\`\`\`

### Endpoints

#### Check Availability
\`\`\`
POST /check
\`\`\`

Request body:
\`\`\`json
{
  "name": "example",
  "domains": ["com", "net", "org"],
  "social": ["twitter", "instagram", "github"]
}
\`\`\`

Response:
\`\`\`json
{
  "results": {
    "domains": {
      "com": false,
      "net": true,
      "org": true
    },
    "social": {
      "twitter": false,
      "instagram": true,
      "github": false
    }
  }
}
\`\`\`

For complete API documentation, visit [isavailable.ai/docs/api](https://isavailable.ai/api).

---

## 7. Deployment

isavailable.ai is optimized for deployment on Vercel:

\`\`\`bash
# Install Vercel CLI
npm install -g vercel

# Deploy to Vercel
vercel
\`\`\`

For production deployment:
\`\`\`bash
vercel --prod
\`\`\`

Alternative deployment options:
- **Netlify**: Compatible with minimal configuration
- **AWS Amplify**: Supported with custom build settings
- **Docker**: Dockerfile included for containerized deployment

---

## 8. Contributing

We welcome contributions from the community! Here's how you can help:

1. **Fork** the repository
2. **Clone** your fork to your local machine
3. **Create** a new branch (`git checkout -b feature/amazing-feature`)
4. **Commit** your changes (`git commit -m 'Add some amazing feature'`)
5. **Push** to the branch (`git push origin feature/amazing-feature`)
6. **Open** a Pull Request

Please read our [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

## 9. Roadmap

We're constantly working to improve isavailable.ai. Here's what's coming next:

- [ ] **User Authentication**: Save and manage your searches
- [ ] **Batch Checking**: Check multiple names at once
- [ ] **Export Functionality**: Download results in CSV/PDF
- [ ] **Domain Registration**: Direct links to register available domains
- [ ] **Name Suggestions**: AI-powered name recommendations
- [ ] **Advanced Analytics**: Insights on name popularity and trends
- [ ] **Browser Extension**: Quick checks from any webpage
- [ ] **Mobile App**: Native iOS and Android applications

---

## 10. License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 11. Acknowledgements

- [Next.js](https://nextjs.org/) - The React framework
- [Tailwind CSS](https://tailwindcss.com/) - CSS framework
- [shadcn/ui](https://ui.shadcn.com/) - UI components
- [Framer Motion](https://www.framer.com/motion/) - Animation library
- [Lucide Icons](https://lucide.dev/) - Beautiful icons
- [Vercel](https://vercel.com/) - Deployment platform

Special thanks to all our [contributors](https://github.com/Mizokuiam/isavailable.ai/graphs/contributors) and early users who provided valuable feedback.

---

## 12. Contact

- **Website**: [isavailable.ai](https://isavailable.ai)
- **Email**: hello@isavailable.ai
- **Twitter**: [@isavailableai](https://twitter.com/isavailableai)
- **GitHub**: [Mizokuiam/isavailable.ai](https://github.com/Mizokuiam/isavailable.ai)

For bug reports and feature requests, please use our [issue tracker](https://github.com/Mizokuiam/isavailable.ai/issues).

---

<div align="center">
  <p>© 2023 isavailable.ai. All rights reserved.</p>
</div>