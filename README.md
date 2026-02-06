# Eldeetech Ltd — Official Website

Live Preview: Deployed on Vercel  
Custom Domain: https://eldeetech.com.ng

---

## About Eldeetech Ltd

Eldeetech Ltd is an integrated Information Technology, Digital Solutions, and Data Consultancy firm based in Nigeria. We deliver end‑to‑end technology services — from software development and digital transformation to data analytics and cloud consulting — empowering businesses and individuals to thrive in a digital economy.

This website serves as our corporate presence and client gateway, showcasing our expertise, service portfolio, and contact channels.

---

## Tech Stack

| Category | Technologies |
|---------|--------------|
| Frontend Framework | React 18 |
| Build Tool | Vite |
| Language | TypeScript |
| UI Components | shadcn/ui |
| Styling | Tailwind CSS |
| Icons | Lucide React |
| Hosting | Vercel |
| Mail Integration | Zoho Mail (SMTP via Nodemailer) |
| Domain | eldeetech.com.ng (Cloudflare DNS) |

---

## Key Features

### Website Experience
- Hero-led homepage with clear primary/secondary calls-to-action
- Services overview cards with hover interactions
- “Why Choose Us” highlights and experience stats
- Client testimonials section
- CTA banner for lead generation
- Responsive navigation with desktop + mobile menu states
- Branded footer with quick links, service list, contact info, and social links

### Core Pages
- **Home**: Hero, services overview, value proposition, testimonials, and CTA
- **About**: Company story, mission, vision, values, and leadership approach
- **Services**: Category-based service catalog with direct contact inquiry links
- **Training**: Programs, learning features, and mentorship details
- **Contact**: Contact cards + form for direct inquiries

### Contact & Email Flow
- Contact form with validation and honeypot spam prevention
- Serverless mail handler with Zoho SMTP (Nodemailer)
- Admin notification email with full request details
- Customer acknowledgement email with generated ticket ID

### Performance & Platform
- Optimized performance with Vite and code-splitting
- Clean routing via React Router
- HTTPS via Vercel and Cloudflare
- SEO-friendly metadata and modern UI components (shadcn/ui + Tailwind CSS)

---

## Screenshots

### Homepage

![Eldeetech homepage](Eldeetech%20Homepage.jpg)

### Autoresponse Email (Ticket Confirmation)

![Eldeetech autoresponse email with ticket ID](Auto%20mail%20edeetech%20response.png)

---

## Local Development

From the repository root:

```
cd eldeetech
npm install

# Start Vite (frontend) and local API (Express) together
npm run dev:all
```

The frontend runs on http://localhost:8080 and proxies API requests to http://localhost:3000.

- API route for mail: POST /api/send-mail
- Local API server source: `eldeetech/api/dev-server.js` (reuses the Vercel handler)

Environment variables for local development go in `eldeetech/.env`:

- ZOHO_USER, ZOHO_PASS
- optional: ZOHO_SMTP_HOST, ZOHO_SMTP_PORT, TO_PRIMARY, TO_CC, EMAIL_TZ, EMAIL_FOOTER_IMAGE_URL

---

## Deploy on Vercel

Project Settings:

- Root Directory: `eldeetech`
- Build Command: `npm run build`
- Output Directory: `dist`
- Install Command: `npm install`

Environment Variables (Project Settings → Environment Variables):

- ZOHO_USER, ZOHO_PASS
- optional: ZOHO_SMTP_HOST, ZOHO_SMTP_PORT, TO_PRIMARY, TO_CC, EMAIL_TZ, EMAIL_FOOTER_IMAGE_URL

API route `/api/send-mail` is implemented at `eldeetech/api/send-mail.js` and deploys automatically as a Vercel Function.
