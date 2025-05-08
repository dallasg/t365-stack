# 🧠 T365 Stack

A modern full-stack starter for building Microsoft 365-powered web apps using the T3 Stack and Microsoft Graph — with everything typed, styled, and deployed.

## 🚀 What is the T365 Stack?

The **T365 Stack** is your toolkit for building productivity tools on top of Microsoft 365, powered by:

- **Next.js (App Router)** — The modern React meta-framework
- **Tailwind CSS + ShadCN UI** — Accessible, fast, beautiful styling
- **tRPC** — End-to-end typesafe APIs (no REST, no GraphQL)
- **Zod** — Schema validation with type inference
- **NextAuth.js** — Secure Azure AD login with Microsoft Graph access
- **Prisma** — Flexible database layer
- **Microsoft Graph API** — Real-time 365 data: calendar, presence, email
- **Vercel** — Fast deploys and edge-ready serverless

---

## ✨ Features

- 🔐 Microsoft SSO with Azure AD
- 📅 Fetch calendar events and Teams presence
- 📝 Add personal notes with Prisma or D1
- ⚡ End-to-end type safety with tRPC and Zod
- 🎨 Modern UI components with ShadCN + Tailwind
- 🌍 Deploy-ready on Vercel

---

## 🧱 Project Structure

```
/src
  /app           → App Router pages
  /components    → ShadCN UI components
  /lib           → Helpers (e.g. fetchGraph.ts)
  /server
    /api         → tRPC routers + context
    /auth        → NextAuth config with Azure AD
    /db          → Prisma client + schema
```

---

## 🧪 Getting Started

1. **Clone & Install**

```bash
git clone https://github.com/yourusername/t365-stack.git
cd t365-stack
pnpm install
```

2. **Set Environment Variables**

```bash
cp .env.example .env
```

Then fill in:

```env
AZURE_AD_CLIENT_ID=
AZURE_AD_CLIENT_SECRET=
AZURE_AD_TENANT_ID=organizations # or your specific tenant ID
NEXTAUTH_SECRET=generate-one
NEXTAUTH_URL=http://localhost:3000
```

3. **Run Locally**

```bash
pnpm dev
```

Open `http://localhost:3000`

---

## 🔐 Azure AD Setup

1. Go to https://portal.azure.com → App Registrations
2. Register your app
3. Redirect URI:
   `http://localhost:3000/api/auth/callback/microsoft-entra-id`
4. Enable Microsoft Graph scopes:
   - `User.Read`, `Presence.Read`, `Calendars.Read`
5. Set **tenantId** in `.env`:
   - Use `organizations` for multi-tenant
   - Use your Tenant ID for internal-only

---

## ☁️ Deployment

This stack is Vercel-ready:

1. Push to GitHub
2. Import to [vercel.com](https://vercel.com)
3. Add environment variables
4. Deploy 🚀

---

## 🤝 Credits

Built with love and caffeine using:

- [Create T3 App](https://create.t3.gg)
- [Microsoft Graph](https://learn.microsoft.com/en-us/graph/)
- [ShadCN UI](https://ui.shadcn.com)
- [NextAuth.js](https://next-auth.js.org)

---

## 📄 License

MIT
