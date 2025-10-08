Welcome to the **template-basilica** repository. 
---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [Architecture & Tech Stack](#architecture--tech-stack)  
4. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
   - [Configuration](#configuration)  
   - [Local Development](#local-development)  
5. [Directory Structure](#directory-structure)  
6. [Deployment](#deployment)  
7. [Contributing](#contributing)  
8. [Security & Compliance](#security--compliance)  
9. [License](#license)  
10. [Contact & Support](#contact--support)  

---

## Project Overview

The **gyvenimo-kelias-template-basilica** repository provides:

- A modular, responsive website template tailored to Basilicas  
- Prebuilt pages: Home, History, Architecture, Pilgrimages, Events, Clergy, Donations, Contact  
- Shared components and global layouts aligned with the Master Site  
- Multilingual readiness (LT / EN / RU) with language-specific routing  
- Seamless integration with Bitrix24 CRM for bookings, donations, and event management  

This template ensures consistency across all Basilica tenants while enabling rapid customization and deployment.

---

## Features

- **Key Pages**  
  - Home with hero, value proposition, CTA  
  - History & Heritage overview  
  - Architectural Highlights gallery  
  - Pilgrimage Routes & Visitor Info  
  - Event Calendar & Registration  
  - Clergy Profiles & Messages  
  - Secure Donation Flow (Bitrix24)  
  - Contact & Location (Google Maps)  

- **Core Modules**  
  - Donation / Online Giving  
  - Event Calendar / Ticketing  
  - Blog / News Feed  
  - Image Gallery & Media  
  - Staff / Leadership Profiles  
  - Social Media Integration  
  - Testimonials & Reviews  
  - FAQ / Help Center  

- **Design & Branding**  
  - Primary Colors: Deep Blue (#1A237E), Gold (#FFD700), White (#FFFFFF)  
  - Typography: Montserrat (headings), Roboto (body)  
  - Flat-style SVG icons and warm-tone photography  

---

## Architecture & Tech Stack

| Layer               | Technology                                    |
|---------------------|-----------------------------------------------|
| Frontend            | Bitrix24 Site Builder, Semantic HTML5, SASS   |
| Shared Components   | SASS variables, SVG icon library              |
| CMS                 | 1C-Bitrix Multi-Site                          |
| CRM & E-Commerce    | Bitrix24 CRM Online Store Enterprise          |
| Middleware (optional)| Django REST Framework, API Gateway           |
| Database            | PostgreSQL (structured), MongoDB (analytics)  |
| CI/CD               | GitHub Actions, Docker                        |
| Hosting             | Linux Home Server / Google Cloud (hybrid)     |
| Containerization    | Kubernetes (optional scaling)                 |

---

## Getting Started

### Prerequisites

- Git 2.20+  
- Node.js 14+ & npm or Yarn  
- Access to Bitrix24 Sites & CRM modules  
- Docker (for containerized builds)  

### Installation

1. **Clone the repository**  
   ```bash
   git clone https://github.com/gyvenimo-kelias/gyvenimo-kelias-template-basilica.git
   cd gyvenimo-kelias-template-basilica
   ```

2. **Install dependencies**  
   ```bash
   npm install
   # or
   yarn install
   ```

### Configuration

1. **Environment variables**  
   Copy and edit the example file:  
   ```bash
   cp .env.example .env
   ```
   Populate:  
   ```
   BITRIX24_WEBHOOK_URL=
   TEMPLATE_ID=BASILICA
   LANGUAGE_DEFAULT=lt
   ```

2. **Bitrix24 Setup**  
   - Import template ZIP via Bitrix24 Sites admin  
   - Map template pages to site structure  
   - Ensure CRM forms (donation, event registration) use webhook URLs  

### Local Development

```bash
npm run dev
```

- Preview at `http://localhost:3000` (or configured port)  
- Editable SASS variables in `src/styles/variables.scss`  
- SVG icons in `src/assets/icons/`  

---

## Directory Structure

```
/
├── .github/                     # CI/CD workflows
├── src/
│   ├── pages/                   # Page templates (home, history, events...)
│   ├── components/              # Shared UI components
│   ├── styles/                  # SASS partials, variables, mixins
│   └── assets/                  # Images, SVG icons
├── .env.example
├── package.json
├── README.md
└── docker-compose.yml           # Optional local containers
```

---

## Deployment

1. Build production assets:  
   ```bash
   npm run build
   ```
2. Package as a Bitrix24 compatible ZIP.  
3. Upload via Bitrix24 Sites → Templates → Import.  
4. Assign template to a new Basilica tenant subdomain.  

---

## Contributing

We welcome contributions! Please:

1. Fork this repository  
2. Create a feature branch: `git checkout -b feature/XYZ`  
3. Commit your changes with clear messages  
4. Push your branch and open a Pull Request  
5. Ensure CI checks pass and add relevant documentation  

Refer to [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

## Security & Compliance

- All data flows comply with GDPR and Lithuanian data-protection standards.  
- Sensitive credentials managed via environment variables.  
- Dependencies are regularly audited for vulnerabilities.  

---

## License

This template is released under the **MIT License**. See [LICENSE](LICENSE) for details.

---

## Contact & Support

For questions or support:

- **Lead Architect:** Gintaras Kazlauskas  
- **Email:** gintaras.kazlauskas@gyvenimo-kelias.lt  
- **GitHub Issues:** https://github.com/gyvenimo-kelias/gyvenimo-kelias-template-basilica/issues  
```
