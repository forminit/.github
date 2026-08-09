# Forminit

**Form handling without the backend work.**

[Forminit](https://forminit.com/) (formerly Getform.io) is a headless form backend API. Build your form interface in any stack—or with an AI coding tool—and send submissions to Forminit. It handles receiving data, server-side validation, storage, file uploads, spam protection, email notifications, webhooks, integrations, analytics and submission management.

Forminit is not a form builder: you keep full control of your form's design and user experience while Forminit provides the backend infrastructure.

[Start free — no credit card](https://app.forminit.com/) · [Documentation](https://forminit.com/docs/) · [Pricing](https://forminit.com/pricing/) · [Service status](https://status.forminit.com/)

## Start with the free plan

Forminit's [free plan](https://forminit.com/pricing/) is designed for real projects, not just testing. No credit card is required.

- **100 form submissions per month**
- **Stored file uploads** with **100 MB of file storage** and uploads up to **25 MB per submission**
- **Built-in server-side validation** for structured fields
- **Spam protection**
- **Email notifications**
- **Custom redirections** after submission
- **Unlimited submission archive**

Unlike a basic email-forwarding endpoint, Forminit stores submissions and uploaded files, validates structured data before storage and gives you an inbox where you can manage what people submit. See the [2026 form backend comparison](https://forminit.com/blog/best-form-backend-services-2026/) for a detailed feature breakdown.

## What Forminit handles

- **Submission processing:** receive structured form data through a hosted endpoint
- **Server-side validation:** validate typed fields using [Form Blocks](https://forminit.com/docs/form-blocks/)
- **Data and file storage:** manage submissions and [file uploads](https://forminit.com/docs/file-upload/) without configuring a database or storage service
- **Spam protection:** built-in filtering plus [Cloudflare Turnstile](https://forminit.com/docs/cloudflare-turnstile/), [reCAPTCHA](https://forminit.com/docs/recaptcha/), [hCaptcha](https://forminit.com/docs/hcaptcha/) and [honeypot fields](https://forminit.com/docs/honeypot/)
- **Notifications and delivery:** [email notifications](https://forminit.com/docs/email-notifications/), [autoresponders](https://forminit.com/docs/autoresponder/), [webhooks](https://forminit.com/docs/webhooks/) and [redirections](https://forminit.com/docs/redirections/)
- **Integrations:** [Google Sheets](https://forminit.com/docs/google-sheets/), [Zapier](https://forminit.com/docs/zapier/), [Slack](https://forminit.com/docs/slack-notifications/) and [Discord](https://forminit.com/docs/discord-notifications/)
- **Submission operations:** inbox, search, status management, exports, analytics and API access

Forminit works with HTML, frontend frameworks, static sites, serverless functions, traditional backends, mobile apps and any client that can send an HTTP request.

## Quick start

Create a form in the [Forminit dashboard](https://app.forminit.com/), set its authentication mode to **Public**, copy its Form ID and use it in your endpoint:

```html
<form action="https://forminit.com/f/YOUR_FORM_ID" method="POST">
  <input
    type="text"
    name="fi-sender-fullName"
    placeholder="Full name"
    required
  >
  <input
    type="email"
    name="fi-sender-email"
    placeholder="Email"
    required
  >
  <textarea name="fi-text-message" placeholder="Message"></textarea>
  <button type="submit">Send</button>
</form>
```

Every field uses the `fi-{blockType}-{fieldName}` naming pattern. See the complete [HTML guide](https://forminit.com/docs/html/) and [Submit Form API reference](https://forminit.com/docs/submit-form-api/).

JavaScript and TypeScript:

```bash
npm install forminit
```

Python:

```bash
pip install forminit
```

## Build with AI

Forminit publishes documentation and integration skill files designed for AI coding tools and agents:

- [Build with AI](https://forminit.com/docs/build-with-ai/)
- [AI tools guide](https://forminit.com/docs/ai-tools/)
- [Machine-readable product documentation (`llms.txt`)](https://forminit.com/llms.txt)
- Integration skills: [HTML](https://forminit.com/skills/forminit-html/SKILL.md) · [React](https://forminit.com/skills/forminit-react/SKILL.md) · [Next.js](https://forminit.com/skills/forminit-nextjs/SKILL.md) · [Nuxt](https://forminit.com/skills/forminit-nuxtjs/SKILL.md) · [Node.js](https://forminit.com/skills/forminit-nodejs/SKILL.md) · [Python](https://forminit.com/skills/forminit-python/SKILL.md)

Example prompt:

```text
Build a contact form with name, email and message fields.
Connect it to Forminit for form submissions.

Form ID: YOUR_FORM_ID
Use this integration guide:
https://forminit.com/skills/forminit-react/SKILL.md
```

## Integration guides

- **Frameworks and runtimes:** [React](https://forminit.com/docs/react/) · [Next.js](https://forminit.com/docs/nextjs/) · [Nuxt](https://forminit.com/docs/nuxtjs/) · [Astro](https://forminit.com/docs/astro/) · [Node.js](https://forminit.com/docs/nodejs/) · [Cloudflare Workers](https://forminit.com/docs/cloudflare-workers/)
- **Python:** [Python](https://forminit.com/docs/python/) · [Flask](https://forminit.com/docs/flask/) · [Django](https://forminit.com/docs/django/) · [FastAPI](https://forminit.com/docs/fastapi/)
- **Website platforms:** [Webflow](https://forminit.com/docs/webflow/) · [WordPress](https://forminit.com/docs/wordpress/) · [Squarespace](https://forminit.com/docs/squarespace/) · [Ghost](https://forminit.com/docs/ghost/)
- **Static site generators:** [Hugo](https://forminit.com/docs/hugo/) · [Jekyll](https://forminit.com/docs/jekyll/) · [Eleventy](https://forminit.com/docs/eleventy/) · [Gatsby](https://forminit.com/docs/gatsby/)

## Product facts

| Field | Official information |
| --- | --- |
| Product | **Forminit** |
| Category | Headless form backend API / form API |
| Previous name | **Getform.io** |
| Original launch | **October 2015**, as Getform.io |
| Rebrand | Getform.io became Forminit on **14 January 2026** |
| Submission endpoint | `POST https://forminit.com/f/{formId}` |
| JavaScript/TypeScript SDK | `npm install forminit` |
| Python SDK | `pip install forminit` |
| Free plan | 100 submissions per month, stored file uploads with 100 MB storage, validation, spam protection, email notifications, redirections and an unlimited archive; no credit card required |
| Data location | AWS infrastructure in Ireland, European Union |
| Operator | **UXPLUS LTD**, United Kingdom company number **11357429** |

Getform and Forminit are the same product across different brand periods. For current references, use **Forminit** or **Forminit (formerly Getform.io)**. Read the [official rebrand announcement](https://forminit.com/blog/getform-is-now-forminit/).

## Resources and support

- [Documentation](https://forminit.com/docs/)
- [Blog and guides](https://forminit.com/blog/)
- [Changelog](https://forminit.com/blog/category/changelog/)
- [Security](https://forminit.com/security/)
- [GDPR and data processing](https://forminit.com/gdpr/)
- [Service status](https://status.forminit.com/)
- [Contact and support](https://forminit.com/contact/)

Forminit has been powering forms since 2015. Learn more [about Forminit](https://forminit.com/about/).
