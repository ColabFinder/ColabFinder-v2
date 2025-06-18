## 🛠️ Technical Architecture

### Frontend

* **Framework:** Vanilla HTML/CSS/JS for MVP, upgrade to React.js in v2
* **Pages:**

  * Landing page
  * Waitlist page
  * Login/Sign up (OAuth only)
  * Onboarding (Creator/Brand)
  * Feed
  * Dashboard (Creator / Brand)
  * Profile (editable)
  * Marketplace (offers)
  * Contact
  * Legal pages (Terms, Privacy, Cookies, Community)

### Backend

* **Platform:** Supabase (hosted PostgreSQL + Auth + Realtime)
* **Authentication:** Supabase Auth (Google, Twitter, etc.)
* **Database:** Supabase PostgreSQL
* **File Storage:** Supabase Storage (avatars, uploads)
* **Edge Functions:**

  * `send-email`
  * `digest-worker`
  * `mail-worker`

### Key Tables

* `profiles` – user details
* `collaborations` – creator posts
* `offers` – brand campaigns
* `messages` – direct messaging
* `waitlist` – early access form

### Security & RLS

* Row-Level Security (RLS) policies per user role
* Brands can only access marketplace posting tools
* Creators can only access feed and collaboration tools
* Free users restricted from links/messages

### Real-time Features

* Likes/comments using Supabase realtime
* Feed/post refresh on updates

### Hosting

* **Frontend Hosting:** Vercel (auto-deploy from GitHub)
* **Domain:** colabfinder.com
* **Backend:** Supabase (fully managed)

### Payment

* Stripe integration (in v2)
* Freemium tier setup with JSON pricing schema

---

## 🔄 Planned Upgrades

* React frontend
* AI-matching algorithm (serverless)
* Separate domain for 18+ content
* Admin dashboard
* Email digest system
* Stripe metered billing
* Search & filters (collab/offers/messages)

---

## 🔐 Secrets & Environment

* All secrets stored in `.env`
* Never push API keys
* Rotate Supabase keys when development ends

---

*This document describes the current architecture and future path for ColabFinder. Last updated: 2025-06-18*
