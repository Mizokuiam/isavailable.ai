<div align="center">
  <img src="github-readme.png" alt="isavailable.ai" width="100%">
</div>

<h1 align="center">isavailable.ai</h1>

<p align="center">Find the perfect name for your brand. Check availability across domains, social media, and more - all in one place.</p>

<div align="center">
  <a href="https://isavailable.ai">Website</a> •
  <a href="https://github.com/Mizokuiam/isavailable.ai">GitHub</a> •
  <a href="https://isavailable.ai/docs">Documentation</a>
</div>

<br>

<div align="center">
  <a href="https://github.com/Mizokuiam/isavailable.ai/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/Mizokuiam/isavailable.ai" alt="License">
  </a>
  <a href="https://github.com/Mizokuiam/isavailable.ai/stargazers">
    <img src="https://img.shields.io/github/stars/Mizokuiam/isavailable.ai" alt="Stars">
  </a>
  <a href="https://github.com/Mizokuiam/isavailable.ai/network/members">
    <img src="https://img.shields.io/github/forks/Mizokuiam/isavailable.ai" alt="Forks">
  </a>
  <a href="https://github.com/Mizokuiam/isavailable.ai/issues">
    <img src="https://img.shields.io/github/issues/Mizokuiam/isavailable.ai" alt="Issues">
  </a>
</div>

---

## Document Overview

1. [Introduction](#1-introduction)
2. [Features](#2-features)
3. [API Documentation](#3-api-documentation)
4. [Roadmap](#4-roadmap)
5. [License](#5-license)
6. [Acknowledgements](#6-acknowledgements)
7. [Contact](#7-contact)

---

## 1. Introduction

**isavailable.ai** is a powerful tool designed to help entrepreneurs, developers, and marketers find the perfect name for their brand or project. With a single search, you can check name availability across multiple domain extensions and social media platforms simultaneously.

Born out of the frustration of manually checking dozens of sites when launching a new project, isavailable.ai streamlines this process into seconds, saving you valuable time and helping you secure your digital identity across the web.

Our mission is to simplify the brand naming process and help creators establish a consistent online presence from day one.

---

## 2. Features

### 2.1 Comprehensive Availability Checking
- 30+ domain extensions (.com, .net, .org, .io, etc.)
- 15+ social media platforms (Twitter, Instagram, GitHub, etc.)
- Real-time verification with multiple methods

### 2.2 Advanced Search Capabilities
- Instant results with high accuracy
- Filter by domains, social media, or available options
- Detailed availability status for each platform

### 2.3 User Experience
- Clean, intuitive interface
- Responsive design for all devices
- Interactive particle network background
- Command menu for quick navigation

### 2.4 Performance & Reliability
- Optimized API with rate limiting
- Result caching for improved performance
- Multiple verification methods for accuracy
- Graceful error handling

---



## 3. API Documentation

isavailable.ai offers a RESTful API for developers who want to integrate availability checking into their own applications.

### 3.1 Base URL
```
https://isavailable.ai/api/v1
```

### 3.2 Authentication
API requests require an API key. You can obtain one by signing up for a Pro or Business plan.

```
Authorization: Bearer YOUR_API_KEY
```

### 3.3 Endpoints

#### 3.3.1 Check Availability
```
POST /check
```

Request body:
```json
{
  "name": "example",
  "domains": ["com", "net", "org"],
  "social": ["twitter", "instagram", "github"]
}
```

Response:
```json
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
```

For complete API documentation, visit [isavailable.ai/docs/api](https://isavailable.ai/api).

---



## 4. Roadmap

We're constantly working to improve isavailable.ai. Here's what's coming next:

### 4.1 Upcoming Features

1. **User Authentication**: Save and manage your searches
2. **Batch Checking**: Check multiple names at once
3. **Export Functionality**: Download results in CSV/PDF
4. **Domain Registration**: Direct links to register available domains
5. **Name Suggestions**: AI-powered name recommendations
6. **Advanced Analytics**: Insights on name popularity and trends
7. **Browser Extension**: Quick checks from any webpage
8. **Mobile App**: Native iOS and Android applications

---

## 5. License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 6. Acknowledgements

### 6.1 Technologies

1. [Next.js](https://nextjs.org/) - The React framework
2. [Tailwind CSS](https://tailwindcss.com/) - CSS framework
3. [shadcn/ui](https://ui.shadcn.com/) - UI components
4. [Framer Motion](https://www.framer.com/motion/) - Animation library
5. [Lucide Icons](https://lucide.dev/) - Beautiful icons

### 6.2 Community

Special thanks to all our [contributors](https://github.com/Mizokuiam/isavailable.ai/graphs/contributors) and early users who provided valuable feedback.

---

## 7. Contact

### 7.1 Official Channels

1. **Website**: [isavailable.ai](https://isavailable.ai)
2. **Email**: hello@isavailable.ai
3. **Twitter**: [@isavailableai](https://twitter.com/isavailableai)
4. **GitHub**: [Mizokuiam/isavailable.ai](https://github.com/Mizokuiam/isavailable.ai)

### 7.2 Support

For bug reports and feature requests, please use our [issue tracker](https://github.com/Mizokuiam/isavailable.ai/issues).

---

<div align="center">
  <p>© 2023 isavailable.ai. All rights reserved.</p>
</div>