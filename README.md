# Rishik Reddy Portfolio Website

Welcome to the repository for my personal portfolio website, showcasing my skills, projects, achievements, and contact information. This project is built using **Next.js** and features a modern, responsive design with light and dark theme switching.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [APIs](#apis)
- [Security and Copyright Note](#security-and-copyright-note)

## Project Overview
This portfolio website serves as a digital resume for Rishik Reddy, highlighting my education, skills, projects, achievements, and work experience. It includes an interactive AI component powered by Gemini 2.0 Flash to answer queries about me and a contact form that sends messages via email.

## Features
- **Responsive Design**: Optimized for both desktop and mobile devices.
- **Light/Dark Theme Switching**: Toggle between light and dark themes with a single click.
- **AI-Powered Q&A**: An AI component (`/src/sections/ai.js`) answers queries about Rishik Reddy, providing smart, context-aware responses.
- **Contact Form**: A form (`/src/sections/contact.js`) to send messages directly to my email via an API.
- **Dynamic Sections**:
  - **Introduction**: Displays personal information and a profile picture (`/src/sections/intro.js`).
  - **Education**: Card-style layout with dynamic background color changes (`/src/sections/education.js`).
  - **Skills**: Pebble-style glowing skills with hover effects and a detailed view (`/src/sections/skills.js`, `/src/sections/skillsViewMore.js`).
  - **Projects**: Stack-of-cards design with live and GitHub links (`/src/sections/projects.js`).
  - **Achievements**: Carousel-style display of accomplishments (`/src/sections/achievements.js`).
  - **Work Experience**: Side-by-side card layout (commented out in current version, `/src/sections/workexp.js`).
  - **Footer**: Quick links, contact info, and social media links (`/src/sections/footer.js`).
- **About Page**: Dedicated page with detailed information about Rishik Reddy (`/src/app/about/page.js`).

## Technologies Used
- **Framework**: Next.js
- **Styling**: CSS Modules, Tailwind CSS (optional, inferred from modern styling practices)
- **Icons**: FontAwesome for theme toggle icons
- **APIs**:
  - Gemini 2.0 Flash for AI-powered Q&A
  - Custom email API for contact form submissions
- **JavaScript Libraries**: React (via Next.js), useState, useEffect for state management and lifecycle handling
- **Deployment**: Vercel (recommended for Next.js projects)

## Installation
To run this project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Set up environment variables**:
   Create a `.env.local` file in the root directory and add the following:
   ```env
   GEMINI_API_KEY=your_gemini_api_key
   EMAIL_API_KEY=your_email_api_key
   ```

4. **Run the development server**:
   ```bash
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000) in your browser to view the website.

## Usage
- **Navigation**: Use the hamburger menu (mobile) or links (desktop) to jump to sections like Skills, Projects, Achievements, and Contact.
- **Theme Toggle**: Click the moon/sun icon in the navbar to switch between light and dark themes.
- **AI Interaction**: Ask questions about Rishik Reddy via the AI section, and it will respond intelligently.
- **Contact Form**: Fill out the form in the Contact section to send a message directly to Rishik's email.

## Project Structure
```
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   ├── aiEndPoint/
│   │   │   │   └── route.js           # API for Gemini 2.0 Flash AI queries
│   │   │   ├── mailSender/
│   │   │   │   └── route.js           # API for sending contact form emails
│   │   ├── about/
│   │   │   ├── page.js                # About page
│   │   │   └── about.module.css       # About page styles
│   │   ├── globals.css                # Global styles
│   │   ├── layout.js                  # Root layout
│   │   ├── page.js                    # Main page binding all components
│   │   └── page.module.css            # Main page styles
│   ├── sections/
│   │   ├── achievements.js            # Carousel-style achievements
│   │   ├── ai.js                      # AI Q&A component
│   │   ├── contact.js                 # Contact form
│   │   ├── education.js               # Card-style education section
│   │   ├── footer.js                  # Footer with links
│   │   ├── intro.js                   # Intro with profile info
│   │   ├── projects.js                # Stack-of-cards projects
│   │   ├── skills.js                  # Pebble-style skills
│   │   ├── skillsViewMore.js          # Detailed skills view (bars and categories)
│   │   ├── workexp.js                 # Work experience (commented out)
│   │   └── css/
│   │       ├── achievements.module.css
│   │       ├── ai.module.css
│   │       ├── contact.module.css
│   │       ├── education.module.css
│   │       ├── footer.module.css
│   │       ├── introDark.module.css
│   │       ├── introLight.module.css
│   │       ├── projects.module.css
│   │       ├── skills.module.css
│   │       ├── skillsViewMore.module.css
│   │       └── workexp.module.css
├── .env.local                         # Environment variables (not tracked)
├── package.json                       # Dependencies and scripts
└── README.md                          # This file
```

## APIs
- **AI Endpoint** (`/src/app/api/aiEndPoint/route.js`):
  Handles incoming queries and outgoing responses to the Gemini 2.0 Flash API for the AI Q&A feature.
- **Mail Sender** (`/src/app/api/mailSender/route.js`):
  Sends emails to Rishik with details (name, email, message) submitted through the contact form.

## Security and Copyright Note
Partial code has been intentionally removed for security purposes and copyright protection. This repository is designed to demonstrate the structure and functionality of my portfolio website, showcasing how it works behind the scenes. Sensitive logic, API keys, and proprietary code are excluded to protect intellectual property and maintain security.

---

Thank you for visiting my portfolio repository
