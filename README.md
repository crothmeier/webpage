# Lazarus Laboratories Consulting — Webpage Repo
Hi! I’m Christopher Rothmeier. This repository contains the source code for my **Lazarus Laboratories Consulting** static website. Below, you’ll find a quick overview of the folder structure, how to run it locally, and how I deploy it to Azure Static Web Apps.

---

## Overview

- **Purpose**  
  This website showcases Lazarus Laboratories Consulting, highlighting our Managed IT Services, cybersecurity solutions, infrastructure consulting, and more—all in a single-page static site.

- **Tech Stack**  
  - **HTML5** and **CSS** for page layout/styles.
  - **Bootstrap 5** (via CDN) for responsive grid and UI components.
  - **Images** are stored locally in the `photos/` folder.

---

## Folder Structure

webpage/ ├── index.html // The main homepage ├── styles.css // Custom CSS styling for the site ├── photos/ // Directory containing all images used by the site │ ├── lazlogo2-draft2.png │ ├── glasses.jpeg │ ├── datacenter.jpeg │ ├── pat.jpg │ └── ... (other images) └── README.md // This file
1. **index.html**: The core content, referencing Bootstrap’s CDN and `styles.css`.
2. **styles.css**: My custom stylesheet for additional layout and styling details.
3. **photos/**: Contains the local images (logos, stock photos, etc.) used throughout the page.
4. **README.md**: Provides project background, structure, and deployment steps.

---

## Usage & Local Development

1. **Clone or Download** this repo:
   ```bash
   git clone https://github.com/crothmeier/webpage.git
Open index.html in your web browser (double-click or drag onto a browser window).
Make sure styles.css and the photos directory are in the same folder level as index.html.
You should see the Lazarus Labs landing page with the hero banner, services columns, testimonials, etc.

Deployment Steps
I’m hosting this on Azure Static Web Apps (or you could use GitHub Pages, Netlify, etc.). My typical workflow:
Push commits from my local machine to the main branch on GitHub.
Azure Static Web Apps picks up the changes automatically (or via GitHub Actions).
The site is published at my custom domain or the default .azurestaticapps.net domain.
Here’s a simplified approach for Azure:
Create an Azure Static Web App in the Azure Portal.
Point it to this GitHub repo (crothmeier/webpage).
On the build settings, if needed, specify:
App location: / (root)
Output location: / (since we’re just hosting static files).
Azure sets up a GitHub Action for continuous deployment.
Now, whenever I commit changes to index.html, styles.css, or add images, Azure automatically rebuilds and deploys the site.

Contact & License
Author: Christopher Rothmeier
Website: lazarus-labs.com
License: This repo is primarily for my own business site. If you want to reuse or adapt any portion, please get in touch.
Thanks for checking out my code! Feel free to open an issue or fork if you have suggestions or improvements.

