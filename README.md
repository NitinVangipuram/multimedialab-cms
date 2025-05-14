# Multimedia Lab CMS

A Strapi-based headless CMS backend for the Emerging Multimedia & AI Lab (EMA) website at IIT Dharwad.

## Overview

This repository contains the Strapi CMS backend that powers the EMA Lab website. It provides content management capabilities through a user-friendly admin interface and serves content to the frontend application.

## Content Types

The CMS includes the following content types:

- **Navbar**: Navbar links configuration
- **Dropdowns**: Dropdown menus for navbar items
- **Footer-links**: Links displayed in the website footer
- **Announcements**: Time-sensitive announcements for the website
- **Gallery**: Media items for the gallery page
- **News**: News articles and updates
- **Pages**: Custom page content for dynamic page creation
- **Publications**: Research papers and publications
- **Research**: Research projects and initiatives
- **Team Members**: Information about lab members
- **ThrustAreas**: Key research focus areas
- **AboutUs**: Content for the About Us page
- **Footer**: Content for the footer information section

## Setup Instructions

### Prerequisites

- Node.js (v14.x or later recommended)
- npm or yarn
- PostgreSQL database

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ema-iitdh/multimedialab-cms.git
   cd multimedialab-cms
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create a `.env` file in the root directory with the following format:
   ```
   HOST=0.0.0.0
   PORT=1337
   APP_KEYS=key1,key2,key3,key4
   API_TOKEN_SALT=your-api-token-salt
   ADMIN_JWT_SECRET=your-admin-jwt-secret
   TRANSFER_TOKEN_SALT=your-transfer-token-salt
   JWT_SECRET=your-jwt-secret
   
   # Database
   DATABASE_CLIENT=postgres
   DATABASE_HOST=your-database-host
   DATABASE_PORT=5432
   DATABASE_NAME=your-database-name
   DATABASE_USERNAME=your-database-username
   DATABASE_PASSWORD=your-database-password
   
   # Cloudinary (for media storage)
   CLOUDINARY_NAME=your-cloudinary-name
   CLOUDINARY_KEY=your-cloudinary-key
   CLOUDINARY_SECRET=your-cloudinary-secret
   ```

4. Start the development server:
   ```bash
   npm run develop
   # or
   yarn develop
   ```

5. Access the admin panel at `http://localhost:1337/admin`


## Admin Guide

After setting up the admin account, you can:

1. Create and manage content for all defined content types
2. Configure user permissions and roles
3. Upload and manage media files through Cloudinary integration
4. Set up webhooks for content update notifications

## Connecting to Frontend

The frontend application should be configured to fetch data from this CMS. Set the following in your frontend environment:

```
REACT_APP_API_ENDPOINT==http://localhost:1337
```
