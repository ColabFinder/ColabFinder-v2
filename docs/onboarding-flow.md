# ColabFinder Onboarding Flow

## Purpose

To ensure an intuitive, role-specific onboarding experience for both Creators and Brands, optimized for AI-powered profile matching and platform engagement.

---

## Entry Points

* **After first successful login** (OAuth via Google/Facebook/etc.)
* Redirect to: `/onboarding.html?role=creator` or `/onboarding.html?role=brand`

---

## Shared Onboarding Steps (All Users)

1. **Session Verification**

   * Validate session from Supabase
   * Retrieve user ID and email

2. **Role Selection (if not already passed as URL param)**

   * Choose: `Creator` or `Brand`

3. **Role-Based Form Display**

   * Load relevant onboarding form fields

4. **Form Submission**

   * Save data to `profiles` table (and `brands` table if brand role)
   * Redirect to: `/dashboard.html` or `/brand-dashboard.html` based on role

---

## Creator Onboarding Fields

### Basic Information

* Full Name *(required)*
* Display Name / Username *(optional)*
* Short Bio *(required, max 280 chars)*
* Country *(required, full list + "Other")*

### Content & Audience

* **Languages Spoken** *(multi-select)*

  * English, Spanish, French, German, Portuguese, Italian, Russian, Arabic, Hindi, Chinese (Simplified), Other → \[Text input]
* **Content Platforms** *(checkboxes)*

  * Instagram, YouTube, TikTok, Twitter/X, Facebook, Twitch, Podcasts, Other → \[Text input]
* **Followers Per Platform** *(dropdown per selected platform)*

  * 0–100, 101–1,000, 1,001–5,000, 5,001–10,000, 10,001–50,000, 50,001–100,000, 100,001–500,000, 500,001+
* **Content Niches** *(multi-select checkboxes)*

  * Beauty & Fashion, Travel & Adventure, Food & Cooking, Health & Fitness, Technology & Gadgets, Lifestyle & Wellness, Personal Finance & Investing, Parenting & Family, Gaming & eSports, Art & Design, Education & Learning, Music & Entertainment, DIY & Crafts, Sustainability & Eco-Friendly Living, Pets & Animals, Other → \[Text input]
* **Audience Age Groups** *(multi-select checkboxes)*

  * 0–12 (Kids), 13–17 (Teens), 18–24, 25–34, 35–44, 45–54, 55–64, 65+

### Collaboration Preferences

* **Collaboration Types** *(multi-select checkboxes)*

  * Sponsored Content, Product Reviews, Guest Blogging, Social Media Takeovers, Joint Giveaways, Co-Hosting Events/Webinars, Collaborative Videos/Podcasts, Cross-Promotions, Affiliate Partnerships, Co-Creation of Products/Services, Influencer Partnerships, Brand Ambassadorships, Content Swaps, Live Streaming Collaborations, Creative Projects (Art, Music, etc.), Other → \[Text input]

### Links & Portfolio

* Instagram, TikTok, YouTube URLs *(optional)*
* Add custom links *(label + URL)*

### Consent

* Checkbox: "I agree to the Terms of Service and Privacy Policy"

---

## Brand Onboarding Fields

### Basic Information

* Company Name *(required)*
* Industry *(dropdown, required)*

  * Beauty & Cosmetics, Fashion & Apparel, Food & Beverage, Health & Wellness, Fitness & Sports, Technology & Electronics, Travel & Tourism, Home & Lifestyle, Entertainment & Media, Finance & Insurance, Automotive, Gaming, Education & E-Learning, Sustainability & Eco-Friendly Products, Pets & Animals
* Company Website *(optional)*
* Country *(required)*
* Contact Email *(autofilled from OAuth)*
* Short Company Description *(optional)*

### Campaign Preferences

* **Campaign Types** *(multi-select checkboxes)*

  * Product Launch, Brand Awareness, Seasonal Promotions, Influencer Takeover, Affiliate Marketing, Event Promotion, Content Series, User-Generated Content Campaign, Social Media Challenge, Email Marketing Collaboration, Giveaway or Contest, Live Streaming Event, Sustainability Campaign, Cause Marketing, Cross-Promotion with Other Brands

### Consent

* Checkbox: "I agree to the Terms of Service and Privacy Policy"

---

## Notes

* All field data will be used for matching engine and visibility filtering.
* Each role’s onboarding completion status should be stored and checked on login.
* If onboarding is skipped or closed, user will be redirected back until complete.

---

## Future Enhancements

* Profile picture upload
* Multi-language support
* Phone number verification

---

**Last updated:** June 18, 2025
