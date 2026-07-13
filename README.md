# Hazem Elbatawy | Full-Stack & Backend API Developer

**Integration Developer | Founder, FolioVista Books | Security Researcher**

![Backend APIs](https://img.shields.io/badge/Backend-APIs-0F766E)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?logo=laravel&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?logo=amazonec2&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-Live-222222?logo=githubpages&logoColor=white)

I build and integrate secure, production-ready backend APIs and full-stack web systems.

My work focuses on connecting services into reliable products using FastAPI, Django, Laravel, React, TypeScript, PostgreSQL, Docker, AWS, and Linux. A security engineer's perspective is built into how I work, with particular attention to authentication, authorization, access control, and data exposure.

## Live Portfolio

[Open the live portfolio](https://zoma00.github.io/hazem-elbatawy-portfolio/)

## Portfolio Focus

- Backend API design, implementation, and extension
- Third-party API and cross-platform service integration
- Full-stack web application delivery
- PostgreSQL and MySQL data modeling
- Dockerized development and deployment workflows
- AWS EC2, Linux, Nginx, and GitHub Pages deployment
- Authentication, authorization, and API access-control review
- Disclosure-safe security research and remediation documentation

## Production Platform — FolioVista Books

I founded [FolioVista Books](https://www.foliovistabooks.com/) as a digital publishing company for digital books, practical guides, manuals, and free sample chapters.

FolioVista Books is my current live production platform and demonstrates product ownership, technical publishing, public deployment, security operations, and direct customer communication.

## Selected Work

| Area | Project | Evidence |
|---|---|---|
| Full-Stack / API | [Vox Estate Agent](https://github.com/zoma00/vox-estate-agent) | FastAPI, React, AI integration, chat, text-to-speech, property management |
| Backend / Integration | [Miando — MT5 Forex Data Integration](https://github.com/zoma00/miando-mt5-forex-integration) | Windows MT5/MQL5 integration with Dockerized Python and PostgreSQL on Linux |
| Backend / API | [Users & Vehicles Forms API](https://github.com/zoma00/django-users-vehicle-forms-api) | Django 5, Django REST Framework, token authentication, middleware, structured logging, tests |
| Backend / Cloud | [Django on AWS EC2](https://github.com/zoma00/django-webpage-access-records-aws-ec2) | Django data application and AWS EC2 deployment documentation |
| Backend / Events | [Django Notifications](https://github.com/zoma00/Django-notifications) | REST APIs, WebSockets, Channels, Celery, Redis, email notifications, tests |
| Backend / API | [FastAPI Bookstore](https://github.com/zoma00/FastAPI-Bookstore) | RESTful CRUD and filtering API built with FastAPI |
| Backend / Admin | [Laravel E-commerce Admin](https://github.com/zoma00/laravel-ecommerce-admin) | Laravel, Jetstream authentication, MySQL, Docker, Blade, catalog administration |
| API Security | [Broken Access Control Case Study](https://github.com/zoma00/bug-bounty-case-study) | Disclosure-safe IDOR/BOLA methodology, evidence handling, and remediation |
| Security Operations | [Linux VPS Security Cases](https://github.com/zoma00/vps-sec-cases) | Hardening, incident response, network troubleshooting, Bash automation |
| Frontend | [SECHIVE](https://github.com/SECHIVEE/SECHIVE) | React, TypeScript, Vite, multi-page physical-security website |
| Frontend | [Reactify](https://github.com/zoma00/Reactify) | React component patterns, Context API, hooks, feature flags, toasts, portal modal |

## Repository Purpose

This repository contains:

- The source deployed as my GitHub Pages portfolio
- Full-stack, backend, deployment, and security project summaries
- Public-safe case-study and security material
- Social-sharing metadata and portfolio preview assets
- GitHub Actions deployment automation

## Deployment Architecture

```text
Push to main
    → GitHub Actions workflow
    → Check out the repository
    → Copy github_pages_boilerplate/ into _site/
    → Upload the GitHub Pages artifact
    → Deploy the live portfolio
```

The deployment workflow publishes the contents of `github_pages_boilerplate/`. Its nested `docs/` directory is intentionally excluded from the Pages artifact and remains repository-only supporting material.

## Repository Structure

```text
hazem-elbatawy-portfolio/
├── .github/
│   └── workflows/
│       └── deploy-pages.yml          # GitHub Pages deployment workflow
├── github_pages_boilerplate/         # Source deployed to GitHub Pages
│   ├── index.html                    # Portfolio homepage
│   ├── case-studies.html             # Public case-study page
│   ├── security-findings.html        # Redacted security findings page
│   ├── styles.css                    # Portfolio styling
│   ├── script.js                     # Client-side interactions
│   ├── social-preview.png            # Social-sharing preview
│   └── docs/                         # Repository-only case-study support files
├── publick_case_sudy/                # Public-safe redacted case-study material
├── tips/                             # Repository maintenance notes
├── GITHUB_PAGES_DEPLOYMENT_GUIDE.md  # Deployment and safety guidance
└── README.md                         # Repository overview
```

The existing `publick_case_sudy/` name is retained because it is the current tracked directory name.

## Important Files

- [`github_pages_boilerplate/index.html`](github_pages_boilerplate/index.html)
- [`github_pages_boilerplate/case-studies.html`](github_pages_boilerplate/case-studies.html)
- [`github_pages_boilerplate/security-findings.html`](github_pages_boilerplate/security-findings.html)
- [`github_pages_boilerplate/styles.css`](github_pages_boilerplate/styles.css)
- [`github_pages_boilerplate/script.js`](github_pages_boilerplate/script.js)
- [`publick_case_sudy/README.md`](publick_case_sudy/README.md)
- [`GITHUB_PAGES_DEPLOYMENT_GUIDE.md`](GITHUB_PAGES_DEPLOYMENT_GUIDE.md)

## Run Locally

The portfolio is static and does not require a build step.

```bash
git clone https://github.com/zoma00/hazem-elbatawy-portfolio.git
cd hazem-elbatawy-portfolio/github_pages_boilerplate
python3 -m http.server 8080
```

Open <http://localhost:8080>.

## Deployment

Changes pushed to `main` trigger `.github/workflows/deploy-pages.yml`.

The workflow:

1. Checks out the repository.
2. Copies `github_pages_boilerplate/` into a temporary `_site/` artifact.
3. Excludes repository-only supporting documents under `docs/`.
4. Uploads the GitHub Pages artifact.
5. Deploys it to the live portfolio URL.

## Disclosure Boundaries

Public security material is intentionally redacted:

- No target or company identifiers
- No endpoint-specific exploit instructions tied to a real finding
- No private report IDs or disclosure links
- No authentication tokens, cookies, session artifacts, or customer data
- No testing outside explicit authorization and scope

The focus is methodology, evidence quality, impact reasoning, remediation, and responsible disclosure.

## Contact

- [FolioVista Books](https://www.foliovistabooks.com/)
- [GitHub](https://github.com/zoma00)
- [LinkedIn](https://www.linkedin.com/in/hazem-el-batawy/)
- [hazem.elbatawy@foliovistabooks.com](mailto:hazem.elbatawy@foliovistabooks.com)
- [contact@foliovistabooks.com](mailto:contact@foliovistabooks.com)
