# Forminit

**The complete backend for all your forms.**

[Forminit](https://forminit.com/) (formerly Getform.io) is a headless form backend API for websites and applications. Build your forms with any stack or AI coding tool. Forminit handles submissions, validation, spam protection, file storage, notifications and workflows.

Keep your own design, frontend logic and hosting. Collect leads, support requests, applications and feedback, then manage and act on every submission from one place.

[Start free — no credit card](https://app.forminit.com/) · [Documentation](https://forminit.com/docs/) · [MCP server](https://forminit.com/docs/mcp/) · [Pricing](https://forminit.com/pricing/) · [Service status](https://status.forminit.com/)

## What you can build with Forminit

- **Contact and support forms:** collect enquiries, route them to the right team and track their status.
- **Lead and quote forms:** capture campaign attribution, record leads in Google Sheets and notify your team when a request meets your criteria.
- **Applications and upload forms:** receive structured answers and files together, with server-side validation and stored attachments.
- **Forms across client websites:** organise projects in workspaces and give colleagues or clients access with defined roles.

## From submission to action

[Workflows](https://forminit.com/docs/workflow/) let you decide what happens after each submission on a visual canvas.

- Branch with **If / else** conditions using form answers, sender details or tracking data.
- Send email notifications and autoresponders, call webhooks, notify Slack or Discord, and add rows to Google Sheets.
- Update submission statuses or move matching submissions to Spam or Trash.
- Inspect action results and errors, then retry an individual failed action.
- Prepare changes in a draft and publish when ready.

For example, a quote form can save every enquiry to Google Sheets, notify Slack when the submitted budget exceeds your threshold, and email the remaining enquiries to your team.

Email notifications, conditions and status actions are available on **Free**. Autoresponders, webhooks, Slack, Discord and Google Sheets require **Pro or higher**.

## Form infrastructure included

| Capability | What it gives you |
| --- | --- |
| [Structured data and validation](https://forminit.com/docs/form-blocks/) | Typed fields with built-in server-side validation. |
| [File uploads](https://forminit.com/docs/file-upload/) | Stored attachments with up to 25 MB of files per submission. |
| Spam protection | Built-in filtering, plus [Turnstile](https://forminit.com/docs/cloudflare-turnstile/), [reCAPTCHA](https://forminit.com/docs/recaptcha/), [hCaptcha](https://forminit.com/docs/hcaptcha/) and [honeypots](https://forminit.com/docs/honeypot/). |
| Submission inbox | Search, filters, statuses, stars and internal notes to manage incoming requests. |
| Attribution and analytics | The JavaScript SDK captures UTM parameters and ad click IDs; form analytics help you understand where submissions come from. |
| [MCP server](https://forminit.com/docs/mcp/) | Connect AI tools to read submissions, manage forms, explore submission data and investigate issues. |
| [Signed webhooks](https://forminit.com/docs/webhooks/) | Forward submission data to your services and verify incoming webhook signatures. |
| [Data retention](https://forminit.com/docs/submission-retention/) | Set how long to keep submissions and automatically delete expired records and their files. |
| [Workspaces](https://forminit.com/docs/workspace/) | Organise teams and client projects with Owner, Admin, Editor and Guest roles. |
| [Custom email sender](https://forminit.com/docs/custom-sender-email-smtp/) | Connect your SMTP provider to send notifications and autoresponders from your own domain. |

Feature availability varies by plan. See [pricing](https://forminit.com/pricing/) for current limits and inclusions.

## Quick start

1. Create a form in the [Forminit dashboard](https://app.forminit.com/).
2. Set its authentication mode to **Public** for this browser example.
3. Replace `YOUR_FORM_ID` with your Form ID:

```html
<form action="https://forminit.com/f/YOUR_FORM_ID" method="POST">
  <label for="name">Full name</label>
  <input id="name" type="text" name="fi-sender-fullName" required>

  <label for="email">Email</label>
  <input id="email" type="email" name="fi-sender-email" required>

  <label for="message">Message</label>
  <textarea id="message" name="fi-text-message" required></textarea>

  <button type="submit">Send</button>
</form>
```

Stored fields use `fi-{blockType}-{fieldName}`. Read the [Form Blocks reference](https://forminit.com/docs/form-blocks/) for supported types.

To receive email alerts, configure an email notification step in your form's **Workflow** and publish it. Submit a test through your form, then check the stored answers and workflow results in the dashboard.

Use the [JavaScript/TypeScript SDK](https://forminit.com/docs/sdk/) for in-page submissions and automatic attribution:

```bash
npm install forminit
```

For Python:

```bash
pip install forminit
```

Forminit also supports **Protected** mode for server-side integrations. Keep API keys on your server. See the [authentication overview](https://forminit.com/docs/#authentication-modes) and [Submit Form API](https://forminit.com/docs/submit-form-api/).

## Build with AI

Give your AI coding tool your Form ID and Forminit's [browser integration guide](https://forminit.com/setup.md):

```text
Connect my website's contact form to Forminit.

Form ID: YOUR_FORM_ID

Keep my existing design, validation and form behaviour.
Use Public browser mode and follow this guide:
https://forminit.com/setup.md
```

The guide covers field mapping, SDK integration, uploads, success and error handling, and checks that preserve your existing form behaviour.

More resources: [Build with AI](https://forminit.com/docs/build-with-ai/) · [AI tools guide](https://forminit.com/docs/ai-tools/) · [Machine-readable documentation](https://forminit.com/llms.txt)

## Connect your AI tools with MCP

The [Forminit MCP server](https://forminit.com/docs/mcp/) connects Claude, ChatGPT, Codex, Cursor, VS Code and other compatible AI tools to your Forminit account. Manage forms and work with submissions in plain language, directly from your chat or coding environment.

- **Read and triage submissions:** find messages, summarise enquiries, update statuses and add team notes.
- **Explore submission data:** count submissions by day, country, city, device or browser.
- **Create and connect forms:** create a form and get integration guidance for your stack.
- **Investigate issues:** check for failed notifications, integrations and workflow runs.

For example, ask:

```text
Create a waitlist form and connect it to my Next.js app.
Summarise this week's contact enquiries.
How many signups came from each country in the last 30 days?
Check my forms for failed notifications and integrations.
```

**MCP server URL:**

```text
https://api.forminit.com/mcp
```

Sign in with your Forminit account through OAuth and approve the requested permissions. No API key required. Available on **all plans, including Free**, with your existing account permissions and plan limits.

[Connect your AI tool →](https://forminit.com/docs/mcp/)

## Start free

No credit card required. The Free plan includes:

- **1 form** and **100 submissions per month**
- **100 MB of file storage**, with up to **25 MB of files per submission**
- Server-side validation and spam protection
- Email notifications and custom redirections
- Workflows with conditions, email notifications and status actions
- MCP server access to work with your forms from compatible AI tools
- An unlimited submission archive; spam is automatically deleted after 30 days

[Compare plans](https://forminit.com/pricing/) for more forms and submissions, integrations, CSV export, REST API access, analytics, retention controls and team features.

## Guides and integrations

- **Frontend:** [HTML](https://forminit.com/docs/html/) · [React](https://forminit.com/docs/react/) · [Next.js](https://forminit.com/docs/nextjs/) · [Nuxt](https://forminit.com/docs/nuxtjs/) · [Astro](https://forminit.com/docs/astro/)
- **Backend:** [Node.js](https://forminit.com/docs/nodejs/) · [Python](https://forminit.com/docs/python/) · [Flask](https://forminit.com/docs/flask/) · [Django](https://forminit.com/docs/django/) · [FastAPI](https://forminit.com/docs/fastapi/) · [Cloudflare Workers](https://forminit.com/docs/cloudflare-workers/)
- **Website platforms:** [Webflow](https://forminit.com/docs/webflow/) · [WordPress](https://forminit.com/docs/wordpress/) · [Squarespace](https://forminit.com/docs/squarespace/) · [Ghost](https://forminit.com/docs/ghost/)
- **Connect your tools:** [Google Sheets](https://forminit.com/docs/google-sheets/) · [Zapier](https://forminit.com/docs/zapier/) · [Slack](https://forminit.com/docs/slack-notifications/) · [Discord](https://forminit.com/docs/discord-notifications/) · [Webhooks](https://forminit.com/docs/webhooks/)
- **AI tools:** [MCP server setup for Claude, ChatGPT, Codex, Cursor, VS Code and more](https://forminit.com/docs/mcp/)

Forminit works wherever you can send an HTTP request, including static sites, serverless functions, mobile apps and custom backends. [Browse all guides](https://forminit.com/docs/).

## About Forminit

Powering forms since **2015**. Getform.io became **Forminit** on **14 January 2026**; it is the same product under a new name. Read the [rebrand announcement](https://forminit.com/blog/getform-is-now-forminit/).

Submission data is hosted on AWS infrastructure in **Ireland, European Union**. Forminit is operated by **UXPLUS LTD**, United Kingdom company number **11357429**.

[About](https://forminit.com/about/) · [Changelog](https://forminit.com/blog/category/changelog/) · [Security](https://forminit.com/security/) · [GDPR and data processing](https://forminit.com/gdpr/) · [Contact and support](https://forminit.com/contact/)
