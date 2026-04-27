# 📖 IRISA CUISINE WEBSITE — SIMPLE GUIDE
### For: The owner and anyone helping to manage the website
### Written simply so everyone can understand

---

## 🌟 PART 1: HOW PEOPLE BOOK YOUR AUNTY & HOW SHE GETS THE MESSAGE

Think of the website like a **paper form at a restaurant**.
When a customer fills in the form and clicks "Send" — your aunty gets a message.

There are **TWO ways** the message reaches her phone:

---

### ✅ WAY 1: WhatsApp (Works RIGHT NOW, Zero Setup)

This is **already working**. No setup needed.

When someone fills the booking form and clicks send:
- The website opens WhatsApp automatically
- A pre-written message with ALL the customer's details appears
- Your aunty just receives it like a normal WhatsApp message on her phone

**Example of what she receives on WhatsApp:**
```
🍽️ BOOKING REQUEST — IRISA CUISINE

👤 Name: Jean Paul Hakizimana
📞 Phone: +250 788 123 456
🎉 Event: Wedding
📅 Date: 2025-08-15
👥 Guests: 100 – 200
💬 Message: Need traditional food please
⏰ Submitted: 24/04/2025, 10:32 AM
```

She sees this, she calls them back. Simple. Done. ✅

**The only thing you MUST change:**
In the file, find this line:
```
https://wa.me/250700000000
```
Replace `250700000000` with her **real WhatsApp number**.
Example: if her number is `+250 788 456 789`, write: `wa.me/250788456789`

---

### 📧 WAY 2: Email to Her Phone (Free Setup — Takes 5 Minutes)

This sends a **beautiful email** directly to her Gmail or any email.
She will get a notification on her phone like a normal email.

**How to set it up (Free — forever):**

**Step 1:** Go to this website on a phone or computer:
👉 **https://www.emailjs.com**

**Step 2:** Click "Sign Up Free" — use her Gmail email to register.

**Step 3:** After logging in, click **"Email Services"** → **"Add New Service"** → choose **Gmail** → connect her Gmail.
Copy the **Service ID** it gives you (looks like: `service_abc123`)

**Step 4:** Click **"Email Templates"** → **"Create New Template"**
In the template, write something like this:
```
Subject: 🍽️ New Booking Request — {{event_type}}

Hello Irisa Cuisine!

You have a new booking request:

Name: {{from_name}}
Phone: {{phone}}
Event: {{event_type}}
Date: {{event_date}}
Guests: {{guest_count}}
Message: {{message}}

Time: {{submitted_at}}

Reply to them quickly! 😊
```
Save the template. Copy the **Template ID** (looks like: `template_xyz789`)

**Step 5:** Click your **Account** → **Public Key** → Copy it (looks like: `aBcDeFgHiJ`)

**Step 6:** Open the website file (`irisa-cuisine-v2.html`) with any text editor (like Notepad).
Find these 3 lines and replace with your real values:
```
const EMAILJS_PUBLIC_KEY  = "YOUR_PUBLIC_KEY_HERE";
const EMAILJS_SERVICE_ID  = "YOUR_SERVICE_ID_HERE";
const EMAILJS_TEMPLATE_ID = "YOUR_TEMPLATE_ID_HERE";
```
Change to look like:
```
const EMAILJS_PUBLIC_KEY  = "aBcDeFgHiJ";
const EMAILJS_SERVICE_ID  = "service_abc123";
const EMAILJS_TEMPLATE_ID = "template_xyz789";
```
Save the file. Done! 🎉

From now on, every booking goes to her email AND her phone gets a notification.

**Cost: FREE forever (up to 200 emails/month on free plan)**

---

## 🌐 PART 2: HOW TO PUT THE WEBSITE ONLINE (VERCEL)

Think of Vercel like a **shop space on the internet** — they give it to you for free.

**Steps:**

1. Go to **https://vercel.com** on a computer
2. Click **"Sign Up"** — use GitHub or just email
3. Once inside, click **"Add New Project"**
4. Choose **"Deploy from file"** or drag the `irisa-cuisine-v2.html` file
5. Vercel gives you a link like: `irisa-cuisine.vercel.app` — that's her website! 🌍

**For a custom name** (like `irisacuisine.com`):
- Buy a domain name from **Namecheap.com** (~$10/year)
- In Vercel, go to Settings → Domains → add your domain

---

## 🔧 PART 3: THINGS TO REPLACE IN THE WEBSITE

Think of the website like a **school exercise book** — some parts have dummy text that needs to be replaced with real information. Below is every part you should update.

---

### 📞 CONTACT INFORMATION (MUST CHANGE FIRST)

Find this in the file and replace:

| What to find | Replace with |
|---|---|
| `+250 700 000 000` | Her real phone number |
| `250700000000` (in WhatsApp links) | Her real number without + or spaces |
| `info@irisacuisine.com` | Her real email address |
| `Kigali, Rwanda` | Her exact neighborhood/area if you want |

---

### 🖼️ PHOTOS & IMAGES (VERY IMPORTANT for Professional Look)

Right now the website uses **colored boxes with emoji** instead of real photos.
This is like a school drawing — it works, but real photos make it 10x better.

**The gallery section** has 5 colored boxes. Replace each one with a real photo.

**How to add a real photo:**

Find this in the code:
```html
<div class="gallery-item gi-1">🎊
```

Replace the emoji with nothing, and add a background image:
```html
<div class="gallery-item" style="background-image: url('photo1.jpg'); background-size: cover; background-position: center;">
```

Then put the photo file in the same folder as the website file.

**What photos to take:**
- 📸 Photo of food spread at a real event
- 📸 Photo of the chef (your aunty) cooking or smiling
- 📸 Photo of a wedding table she catered
- 📸 Photo of drinks display
- 📸 Photo of guests eating happily

Even phone photos work great if the lighting is good!

---

### 👩‍🍳 THE "ABOUT" CHEF PHOTO

Find this section:
```html
<div class="about-photo-bg">
  🧑‍🍳
```

Replace `🧑‍🍳` with nothing, and add her real photo:
```html
<div class="about-photo-bg" style="background-image: url('aunty-photo.jpg'); background-size: cover; background-position: top center;">
```

A nice photo of her in the kitchen or holding food is perfect here.

---

### 📝 THE BUSINESS STORY (About Section)

Find the paragraph that starts with:
> *"Kuri Irisa Cuisine Ltd, twemera ko ibirori byose..."*

This is a dummy description. Replace it with **her real story**:
- When did she start cooking professionally?
- What makes her food special?
- What is she proud of?

Example real story:
> *"Irisa Cuisine Ltd yashinzwe na [Her Name] mu 2018 nyuma y'imyaka myinshi yo guteka ibirori by'abagenzi n'abaturanyi. Urukundo rwe rwo guteka rwatangiye akiri muto..."*

---

### 📊 THE STATISTICS NUMBERS

Find these numbers:
```
350+   →  Events Catered
6+     →  Years Experience
1200+  →  Happy Guests
98%    →  Client Satisfaction
```

Replace them with **her real numbers**. If she's not sure, use honest estimates.
If she's new, use smaller numbers like:
- `50+` events, `2+` years, `300+` guests, `95%` satisfaction

**Never lie about numbers** — customers will ask questions!

---

### ⭐ TESTIMONIALS (Customer Reviews)

The 3 reviews shown are **fake (dummy) reviews** — just to show how it looks.

Replace them with **real reviews** from people she has cooked for.
Ask 3-5 of her past clients to give her a short review:

> *"Ask your friends/family who ate your food to write 2-3 sentences about how good it was."*

Get their:
- Real first name + last name initial (e.g. "Amina K.")
- What type of event you cooked for them
- Their short honest review

---

### 🍽️ THE MENU ITEMS

The menu has dishes like "Isambaza Ikonjewe" and "Pilau ya Buffet".

Replace these with **her actual signature dishes** — the food she is most famous for and that she actually cooks for events.

For each dish, update:
- The **emoji** (find one that matches)
- The **name** of the dish
- A **short description** (1-2 sentences)

---

### 📅 THE YEAR IN FOOTER

Find:
```
© 2025 Irisa Cuisine Ltd.
```
This is fine for now. Update the year every January.

---

## 🎨 PART 4: THINGS YOU DO NOT NEED TO TOUCH

These are working perfectly and you should leave them alone:

| Part | Why Leave It |
|---|---|
| The green colors | They match the logo perfectly |
| The animations | Scroll effects, floating foods, etc. |
| The language switcher | Kinyarwanda, Swahili, English, French |
| The mobile layout | Already optimized |
| The fonts | Professional and elegant |
| The booking form | Already connected to WhatsApp |
| The navbar | Already scrolls and sticks |
| The WhatsApp floating button | Already works |

---

## 📱 PART 5: HOW THE LANGUAGE SWITCHER WORKS

At the very top of the website, there are 4 buttons:
```
🇷🇼 Kinyarwanda  🇰🇪 Kiswahili  🇬🇧 English  🇫🇷 Français
```

When a visitor clicks any button, the **entire website** changes language immediately.

The **default language is Kinyarwanda** — so Rwandan visitors see everything in their language first.

If you want to add more languages in the future, ask a developer — it's a simple copy-paste of the translation list.

---

## 🚀 PART 6: AFTER YOU GO LIVE — CHECKLIST

Before sharing the link with people, check these:

- [ ] ✅ WhatsApp number is updated (test it by submitting the form yourself)
- [ ] ✅ Email address is updated
- [ ] ✅ At least 3 real photos added (gallery or about section)
- [ ] ✅ Real testimonials from at least 2-3 people
- [ ] ✅ Statistics match her real numbers
- [ ] ✅ EmailJS is set up (or WhatsApp fallback is working)
- [ ] ✅ Business name/year in footer is correct
- [ ] ✅ Website loads fast on your phone (test on mobile data, not WiFi)

---

## 💡 PART 7: TIPS FOR MAKING IT EVEN BETTER (Future)

These are not urgent but will make the website even more powerful:

1. **Add Google Maps location** — so customers can find her exactly
2. **Add real food photos** — take 10 good photos at the next event you cater
3. **Add a price range section** — "Starting from X,000 Rwf per person" builds trust
4. **Post the website link on Instagram/Facebook** — tell people to book online
5. **Ask every client to leave a Google Review** — builds credibility fast
6. **Add a "Packages" section** — e.g. Small (50 people), Medium (100-200), Large (500+)

---

## 📞 QUICK REFERENCE — KEY THINGS TO CHANGE

```
1. WhatsApp Number:   250700000000  →  her real number
2. Email:             info@irisacuisine.com  →  her real email
3. Phone display:     +250 700 000 000  →  her real number (nicely formatted)
4. Chef photo:        emoji 🧑‍🍳  →  her real photo
5. Gallery photos:    colored boxes  →  real event photos
6. Story paragraph:   dummy text  →  her real story
7. Stats numbers:     350+, 6+, 1200+  →  her real numbers
8. Reviews:           fake names  →  real client reviews
9. Menu items:        example dishes  →  her actual dishes
10. EmailJS keys:      "YOUR_..._HERE"  →  real keys from emailjs.com
```

---

*This document was prepared for Irisa Cuisine Ltd.*
*Website Version 2.0 — Multilingual · Mobile-First · Booking Enabled*
