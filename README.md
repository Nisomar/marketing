# Nisomar Marketing Website

A static HTML marketing website for Nisomar's maritime data analytics and API services platform.

## About

This is the marketing landing page for Nisomar, a company providing maritime intelligence services including:

- Port congestion analytics
- Port turnaround statistics  
- Maritime routes optimization
- Distance calculator services
- Vessel tracking and analytics
- Port statistics and logistics solutions

The website showcases Nisomar's API services powered by AIS (Automatic Identification System) data for maritime operations optimization.

## Features

- **Responsive Design**: Built with Tailwind CSS for mobile-first responsive layout
- **Modern UI**: Clean, professional maritime-themed design
- **API Documentation**: Information about available maritime data endpoints
- **Customer Testimonials**: Social proof from satisfied clients
- **Contact Forms**: Easy ways for potential customers to get in touch
- **Demo Content**: Includes video demonstrations (routes_demo.mp4, ship_analytics.mov)

## Technology Stack

- **HTML5**: Semantic markup structure
- **Tailwind CSS**: Utility-first CSS framework via CDN
- **Font Awesome**: Icon library for UI elements
- **JavaScript**: Interactive elements and configuration

## Project Structure

```
├── index.html          # Main landing page
├── robots.txt          # Search engine crawling instructions  
├── sitemap.xml         # Site structure for search engines
├── routes_demo.mp4     # Maritime routes demonstration video
├── ship_analytics.mov  # Ship analytics demonstration video
├── LICENSE             # Project license
└── README.md           # This file
```

## How to Make Changes

### Prerequisites

- A text editor or IDE (VS Code recommended)
- Basic knowledge of HTML, CSS, and JavaScript
- A local web server for testing (optional but recommended)

### Making Content Changes

1. **Text Content**: Edit the HTML content directly in `index.html`
   - Company descriptions, feature lists, and testimonials are in standard HTML tags
   - Update meta descriptions and keywords in the `<head>` section for SEO

2. **Styling Changes**: The site uses Tailwind CSS classes
   - Modify existing classes or add new ones directly in the HTML
   - Custom color scheme is defined in the Tailwind config within the `<script>` tag
   - Ocean-themed color palette: `ocean-50` through `ocean-900`

3. **Adding New Sections**: 
   - Follow the existing HTML structure and Tailwind classes
   - Maintain responsive design patterns (`md:`, `lg:` prefixes)
   - Keep consistent spacing and typography scales

4. **Navigation Updates**:
   - Modify the navigation links in the header section
   - Update both desktop and mobile menu versions
   - Ensure anchor links correspond to actual page sections

5. **Contact Information**:
   - Update contact forms, email addresses, and social links
   - Modify the footer contact details


### Deployment

Since this is a static site, deployment(making changes) steps include:
- **Traditional Web Hosting**:
    - push changes to github
    - login to conscomserver
    - navigate to  /usr/share/nginx/html/marketing/
    - git pull
    - refresh the page(refresh cache if no changes seen ctrl/cmd+shift+r)


### Troubleshooting
 # if the website is not reachable its probably due to the ssl needing updating. Conscom and nisomar domains use free letsencrypt certificate, these need be updated every 6 months
    # To renew the certificates you need to stop nginx first
    ```
    sudo systemctl stop nginx
    sudo certbot renew 
    sudo systemctl start nginx
    ```
    # this will renew the certificates for conscom and nisomar