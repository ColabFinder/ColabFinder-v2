# ColabFinder MVP - User Stories

## 👤 User Types

* **Creator**: A content creator looking for collaboration or brand sponsorship.
* **Brand**: A business or agency looking to collaborate with content creators.
* **Guest**: Unauthenticated visitor browsing limited site content.

---

## 🎯 Core User Stories (MVP)

### Creator Stories

#### 1. Sign Up / Log In

* As a creator, I want to sign up quickly using Google (or another OAuth provider), so I can access the platform without creating a new password.

#### 2. Onboarding

* As a new creator, I want to fill out onboarding fields to define my niche, content platforms, audience demographics, etc., so I can get matched with relevant brands and collaborators.

#### 3. View Feed

* As a creator, I want to see a feed of collaboration posts from other creators and promotional offers from brands, so I can find opportunities.

#### 4. Create a Collaboration Post

* As a creator, I want to create a post describing the type of collaboration I’m looking for, so other creators or brands can find and contact me (if I have a paid plan).

#### 5. View Brand Offers (Marketplace)

* As a creator, I want to browse offers from brands in the Marketplace tab.

#### 6. Apply to Brand Offer

* As a creator, I want to apply to offers I'm interested in so I can start a potential partnership.

#### 7. View Profile

* As a creator, I want to manage and customize my public profile, so it reflects my personality and past collaborations.

#### 8. Messaging (Paid Only)

* As a paid creator, I want to message other users (creators or brands) so I can discuss collaborations.

#### 9. See Engagement Limits

* As a free user, I want to know what features are locked so I’m encouraged to upgrade.

---

### Brand Stories

#### 1. Sign Up / Log In

* As a brand, I want to sign up using Google OAuth or other providers so I can quickly create an account.

#### 2. Onboarding

* As a brand, I want to provide campaign and company details during onboarding so the platform can recommend suitable creators.

#### 3. Post an Offer

* As a brand, I want to post a collaboration offer so creators can apply.

#### 4. View Applications

* As a brand, I want to review and manage applications from creators.

#### 5. View Creator Feed (Read-Only)

* As a brand, I want to view the creator feed to see collaboration trends and featured creators (read-only).

#### 6. Message Creators (Paid Only)

* As a brand with a paid plan, I want to directly message creators about opportunities.

#### 7. Manage Dashboard

* As a brand, I want a dashboard where I can manage my campaigns, offers, applicants, and messages.

---

### Guest Stories

#### 1. View Landing Page

* As a visitor, I want to understand what ColabFinder does so I can decide to join.

#### 2. Join Waitlist

* As a visitor, I want to join the waitlist to be notified when the platform launches.

---

## 🔐 Role-Based Access Summary

| Page / Feature        | Creator (Free) | Creator (Paid) | Brand (Free)  | Brand (Paid)  | Guest |
| --------------------- | -------------- | -------------- | ------------- | ------------- | ----- |
| View Feed             | ✅              | ✅              | 👁️ Read-only | 👁️ Read-only | ❌     |
| Create Collaboration  | ✅              | ✅              | ❌             | ❌             | ❌     |
| Post Brand Offer      | ❌              | ❌              | ✅             | ✅             | ❌     |
| Apply to Offers       | ✅              | ✅              | ❌             | ❌             | ❌     |
| View Marketplace      | ✅              | ✅              | ✅             | ✅             | ❌     |
| Message Other Users   | ❌              | ✅              | ❌             | ✅             | ❌     |
| Profile Customization | ✅              | ✅              | ✅             | ✅             | ❌     |
| Dashboard Access      | ✅              | ✅              | ✅             | ✅             | ❌     |

---

## 📌 Notes

* All user stories are subject to expansion in post-MVP development.
* Features like notifications, rating/review systems, and in-app scheduling may be added later.

---

**Next Suggested File**: `onboarding-flow.md`
