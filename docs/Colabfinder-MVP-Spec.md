# ColabFinder MVP Specification

## 🎯 Purpose

ColabFinder is a creator-brand collaboration platform designed to make influencer partnerships seamless. The MVP focuses on user onboarding, profile creation, collaboration posting, marketplace browsing, and monetized communication features.

---

## 🧠 Target Users

* **Creators**: Influencers, content creators, and professionals looking for collaborations.
* **Brands**: Businesses and agencies offering campaigns or partnerships.

---

## 🧱 Tech Stack

* **Frontend**: HTML, CSS, JavaScript (Vanilla)
* **Backend**: Supabase (auth, database, real-time)
* **Auth**: Supabase Auth with Google (email optional)
* **Hosting**: GitHub Pages (for MVP)

---

## 🌐 Page-by-Page Layout

### 1. Landing Page

* Hero text, short CTA, “Join Waitlist” form
* Description of platform benefits
* Link to waitlist.html

### 2. Waitlist Page (`waitlist.html`)

* Collects email and role (creator/brand)
* Confirmation message
* Stored in Supabase `waitlist` table

### 3. Login / Register

* Google OAuth login
* Redirect to onboarding on first login

### 4. Onboarding

* Role selection (creator or brand)
* Dynamic form based on role

  * **Creator Mandatory Fields**:

    * Full Name
    * Display Name
    * Short Bio
    * Country (all countries, dropdown + "Other")
    * Languages Spoken (checkbox)
    * Content Platforms (checkbox + "Other")
    * Followers per Platform (dropdown ranges)
    * Content Niches (checkbox + "Other")
    * Audience Age Groups (checkbox, includes "Kids")
    * Collaboration Types (checkbox + "Other")
    * Consent to Terms checkbox
  * **Brand Mandatory Fields**:

    * Brand Name
    * Contact Person Name
    * Industry (preset options)
    * Campaign Type (preset options)
    * Campaign Goals (textarea)
    * Website/Socials (optional)

### 5. Feed Page (`feed.html`)

* Real-time posts from creators and brands
* Like, comment (paid users only)
* Brand posts marked as “Promoted”

### 6. Dashboard

* Personalized view: collaborations, stats
* Link to edit profile
* Add/edit collaboration post

### 7. Profile Page (View-only)

* Display full info + feed
* Social links visible only to paid users

### 8. Marketplace

* Campaigns from brands
* Apply (paid only)
* Saved offers

### 9. Messages

* In-app messaging between users (paid only)
* Safe word filters to block external links/emails

### 10. Legal Pages

* `/privacy.html`
* `/terms.html`
* `/cookie.html`
* `/community.html`
* `/contact.html`

---

## 💳 Freemium Plan Structure

### Free Plan (for Creators & Brands)

* View feed and marketplace
* View limited profile info
* No messages or social links
* No collaboration applications

### Paid Plan

* Send messages
* View all profile info and links
* Apply to collaborations
* AI-powered matchmaking
* Boosted profile in search

---

## 🔒 Access Logic Map (Role + Plan)

| Feature                          | Creator (Free) | Creator (Paid) | Brand (Free)      | Brand (Paid) |
| -------------------------------- | -------------- | -------------- | ----------------- | ------------ |
| View Feed / Collaborations       | ✅              | ✅              | ✅ (Limited)       | ✅ (Full)     |
| Post in Feed                     | ✅              | ✅              | ✅ (Promoted only) | ✅            |
| View Other Users' Profiles       | ✅ (Limited)    | ✅ (Full)       | ✅ (Limited)       | ✅ (Full)     |
| See Social Links (Bio/Portfolio) | ❌              | ✅              | ❌                 | ✅            |
| Send Messages                    | ❌              | ✅              | ❌                 | ✅            |
| Apply to Collaborations          | ❌              | ✅              | ❌                 | N/A          |
| View Marketplace Offers          | ✅              | ✅              | ✅                 | ✅            |
| Post Marketplace Offers          | ❌              | ❌              | ❌                 | ✅            |
| Dashboard (Own Stats & Posts)    | ✅              | ✅              | ✅                 | ✅            |
| Search & Filters (Advanced)      | ❌              | ✅              | ❌                 | ✅            |
| Access to AI Matching            | ❌              | ✅              | ❌                 | ✅            |

---

## 🧠 Smart Engagement Without Bypass

* **Blur links** and disable click for free users
* **“Upgrade to connect”** banners on locked features
* **Filter out emails/usernames** in messaging
* **Bookmark & Save features** for free users to preview but not act

---

## ✅ MVP Milestones (Phases)

### Phase 1 (Complete or In Progress)

* ✅ Waitlist System (Supabase table + email)
* ✅ User Auth with Supabase
* ✅ Role-based onboarding forms
* ✅ Feed with post & like support
* ✅ Dashboard basic view

### Phase 2 (Next)

* ⏳ Marketplace CRUD
* ⏳ Messaging System with filters
* ⏳ Freemium plan enforcement
* ⏳ Stripe integration

### Phase 3 (After MVP)

* 🔜 AI Matching System
* 🔜 Notifications & real-time messaging
* 🔜 Advanced analytics (creator stats)

---

Let me know if you’d like this exported into Markdown, PDF, or uploaded directly to your GitHub `docs/` folder.
