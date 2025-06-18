# ColabFinder v2

Welcome to the official repository for **ColabFinder v2**, a creator collaboration and brand partnership platform. This project is a complete rebuild of the original MVP, focused on clarity, structure, performance, and future scalability.

---

## 🚀 Project Vision
ColabFinder helps **content creators** and **brands** connect, collaborate, and monetize their influence — all in one centralized, AI-powered platform.

Key features:
- Creator + Brand onboarding with role-specific dashboards
- Public creator feed and collaboration posts
- Brand campaign offers via the marketplace
- AI-powered matching and smart filtering
- Waitlist and early access collection
- Freemium model (messaging and contact restricted for free users)

---

## 🧱 Tech Stack

### Frontend
- HTML + Tailwind CSS
- Vanilla JS (modularized)
- Hosted on [Vercel](https://vercel.com)

### Backend
- [Supabase](https://supabase.com):
  - Auth (OAuth via Google, Twitter, etc.)
  - PostgreSQL DB
  - Realtime (likes/comments)
  - Edge Functions (email, AI, etc.)

### External
- Stripe (Freemium/Subscription plans)
- Google APIs (YouTube OAuth scopes)

---

## 🗂 Directory Structure

```bash
colabfinder-v2/
├── frontend/                # Public site & dashboard
│   ├── public/             # HTML pages, assets
│   ├── src/                # Scripts, modules, utils
│   └── styles/             # Global CSS
├── backend/
│   ├── supabase/           # DB schema, RLS, SQL
│   ├── edge-functions/     # Supabase Edge Functions
├── docs/
│   ├── ColabFinder-MVP-Spec.md
│   └── wireframes/
├── .env.example            # Environment variable template
└── README.md               # This file
```

---

## 🧪 Local Development

1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/colabfinder-v2.git
cd colabfinder-v2
```

2. Set up your environment
```bash
cp .env.example .env
```

3. Link Supabase project
```bash
npx supabase link --project-ref your-project-id
```

4. Start local dev
```bash
npm run dev
```

---

## 📄 License
This project is under the [MIT License](LICENSE).

---

## 👋 Contact
Built with ❤️ by Oleg and ChatGPT.

For early access, questions, or collaboration: **colabfinderhq@gmail.com**
