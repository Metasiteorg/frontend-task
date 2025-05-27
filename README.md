# Frontend Developer Task

![Preview](./assets/preview.png)

## Overview

Implement a responsive contact management application based on the provided design. The application should support both desktop and mobile layouts, user authentication, and dynamic data management with filtering and pagination capabilities.

## Implementation Options

You have **two options** to complete this task:

### Option 1: Build from Scratch

- Create a new application using **React** or **NextJS** (your choice)
- Follow the Figma design specifications exactly
- Implement all core features from the requirements
- Demonstrate your ability to architect a clean, scalable solution

### Option 2: Refactor Existing Application

- Use the provided NextJS application (`./assets/people-app.zip`)
- **Current Issues to Address:**
  - Design misalignments and missing elements compared to Figma specs
  - Missing lazy loading/infinite scroll implementation
  - Poor code modularization and component reusability
  - Performance issues
  - Architecture and code quality improvements needed
- **Your Tasks:**
  - Refactor and clean the codebase
  - Fix design inconsistencies to match Figma specifications
  - Implement missing core features (lazy loading, proper filtering, etc.)
  - Improve code architecture and maintainability
  - Be prepared to explain your refactoring decisions and improvements

**Choose the option that best demonstrates your skills and approach to development.**

## Design Files

- **Figma Design**: `./assets/design.fig`
- **Preview Image**: `./assets/preview.png`
- **NextJS Application**: `./assets/people-app.zip` - Unfinished NextJS project (see Implementation Options above)

## API Documentation

**Base URL**: `https://metasite-fe-task-api.azurewebsites.net/api/v1`  
**Swagger Documentation**: [https://metasite-fe-task-api.azurewebsites.net/api/docs/v1](https://metasite-fe-task-api.azurewebsites.net/api/docs/v1)

### Available Endpoints

#### Authentication

- `POST /login` - User authentication
- `POST /refresh` - Refresh authentication token

#### Data Management

- `GET /list` - Get contact list (auth required)
  - **Query Parameters:**
    - `page` (integer, default: 1) - Page number
    - `limit` (integer, default: 10, max: 100) - Number of items per page
    - `country` (string) - Filter by exact country match
    - `city` (string) - Filter by partial city match (case-insensitive)
    - `fullName` (string) - Filter by partial full name match (case-insensitive)
- `GET /list-item?id={id}` - Get specific contact details (auth required)
  - **Query Parameters:**
    - `id` (integer, required) - Item ID

### Authentication Flow

- Login with credentials to receive access and refresh tokens
- Use access token in Authorization header: `Bearer {token}`
- Implement token refresh logic for expired tokens

**Auth Credentials:**

- Username: `metasite`
- Password: `frontend-task`

## Technical Requirements

### Core Features

- **Authentication System**: Login functionality with token management
- **Contact List**: Infinite scroll/lazy loading implementation
- **Filtering**: Search by name, city, and country
- **Routing**: Client-side navigation between views
- **Responsive Design**: Support for both desktop and mobile layouts
- **Contact Details**: View individual contact information

### Technology Stack

- **Framework**: React or NextJS (your choice for Option 1, NextJS for Option 2)
- **Language**: TypeScript
- **Browser Support**: Latest Chrome only
- **Version Control**: GitHub
- **Deployment**: GitHub Pages (optional)

## Evaluation Criteria

**Important**: The solution should closely match the Figma design and look visually similar. However, it does not need to be pixel-perfect - we won't penalize small pixel misalignments. Our primary focus is on **code quality, architecture, and implementation approach** while maintaining a design that follows the Figma specifications.

### Primary Focus Areas

- **Scalability & Maintainability** - Consistent spacing system and design tokens, theme variables, component reusability
- **Clean Code & Architecture** - Proper modularization, React/TypeScript best practices
- **Configuration & Tooling** - ESLint and Prettier setup with custom rules, TypeScript configuration
- **Data Management** - Infinite scroll/lazy loading implementation, efficient state management
- **Filtering & Search** - Multiple filter criteria support, filter state management
- **Routing** - URL state management
- **Authentication Logic** - Login/logout functionality, access token handling, refresh token logic (bonus)

### Additional Points

- **Accessibility** - Semantic HTML structure, ARIA labels and roles, keyboard navigation support
- **SEO** - Meta tags optimization, structured data
- **Testing**

## Submission Guidelines

### Requirements

1. **Source Code**: Public GitHub repository
2. **Deployment**: Live demo on GitHub Pages or similar platform (optional)
3. **Documentation**: Clear setup and run instructions

### Submission Process

Send your submission to **jobs@metasite.net** including:

- GitHub repository link
- Live demo URL (optional)
- Brief description of your implementation approach
- Any additional features or optimizations implemented

## Getting Started

### For Both Options:

1. Download the Figma design file from `./assets/design.fig`
2. Open the design file in Figma to review the layouts and specifications
3. Create a new GitHub repository for your implementation

### Option 1: Build from Scratch

4. Set up your development environment with React or NextJS + TypeScript
5. Implement the application following the requirements using our API and design
6. Deploy to GitHub Pages (optional)
7. Submit your solution

### Option 2: Refactor Existing Application

4. Extract and examine the provided NextJS application from `./assets/people-app.zip`
5. Analyze the current codebase and identify areas for improvement
6. Refactor the application to meet all core feature requirements
7. Fix design inconsistencies and implement missing functionality
8. Deploy to GitHub Pages (optional)
9. Submit your solution with detailed refactoring explanations

---

**Note**: While this is a focused task, approach it as if building a foundation for a larger application. Demonstrate your ability to create maintainable, scalable code that could grow into a comprehensive contact management system.
