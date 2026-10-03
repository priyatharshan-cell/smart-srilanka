# 📱 APEX MOBILE — Premium Mobile Phone E-Commerce Website

A high-performance, real-world electronics and smartphone retail e-commerce platform built with **React 18 + Vite + Tailwind CSS**. 

Designed for scalability, zero-friction customization, instant Vercel deployment, and seamless backend/payment gateway integrations.

---

## 🚀 Key Features

- **Flagship Hero & Showcase**: Interactive flagship switcher featuring Apple iPhone 16 Pro Max, Samsung Galaxy S24 Ultra, and Google Pixel 9 Pro XL with dynamic glow animations and live specs.
- **Data-Driven Architecture**: Centralized `shopConfig.js` and `products.js` allow updating shop name, phone number, currency, colors, banners, and phones in seconds without touching layout components.
- **Dynamic Multi-Attribute Search**: Real-time searching across brand, model name, storage, RAM, colors, network type, and features with instant suggestions dropdown and empty state recommendations.
- **Advanced Filtering & Sorting**:
  - **Brands**: Apple, Samsung, Google, OnePlus, Xiaomi, Oppo, Vivo, Realme, Honor, Nothing, and Accessories
  - **Price Tiers**: Under £200, £200–£400, £400–£600, £600–£800, £800+
  - **Storage**: 64GB, 128GB, 256GB, 512GB, 1TB
  - **RAM**: 4GB, 6GB, 8GB, 12GB, 16GB
  - **Quick Toggles**: In Stock only, On Sale / Deals, New Arrivals, Best Sellers
  - **Sorting**: Featured, Price: Low to High, Price: High to Low, Newest Arrivals, Customer Rating, Biggest Discount
  - Responsive desktop sidebar + smooth slide-over mobile filter drawer
- **Product Details View**:
  - Multi-image gallery with zoom lightbox and thumbnail selector
  - Color swatches with live color naming
  - Storage & RAM variant selectors
  - Quantity controls (- / +)
  - Tabbed specification sheet: Overview, Technical Specs, Key Features, Customer Reviews, UK Delivery, 2-Year Warranty
  - Customers Also Bought & Related Phones carousels
  - Mobile sticky bottom action bar for frictionless ordering
- **Shopping Cart**:
  - Slide-over drawer and standalone cart view
  - Real-time quantity steppers, item options, and trash deletion
  - Promotional coupon codes (`SAVE50`, `WELCOME10`, `FLASH35`)
  - Free delivery progress meter (`Add £X more for FREE Delivery`)
  - Full `localStorage` persistence across page reloads
- **Checkout Experience**:
  - Customer contact details, delivery address validation
  - Delivery speed selector (Standard Tracked, Next-Day Express, Store Click & Collect)
  - Card payment simulation with security checks
  - Stripe / PayPal / Apple Pay / Klarna abstraction hooks
  - Instant order receipt screen with Order ID, printable invoice, and admin synchronization
- **Admin Inventory Dashboard**:
  - Accessible via the **Admin** button in navigation or `/admin`
  - Real-time KPI cards: Total Products, Orders, Recorded Revenue, Active Customers, Low-Stock Alerts
  - Product CRUD: Add product, Edit price/stock/specs/image, Delete product
  - Customer orders history log
  - Discount codes manager
  - Live configuration preview
- **Promotions & Deals**:
  - Flash Sale banner with live ticking Countdown Timer (Hours : Mins : Secs)
  - Badges: `SALE`, `NEW`, `BEST SELLER`, `LOW STOCK`
- **Official Accessories**: Cases, 100W GaN chargers, wireless earbuds, smartwatches, power banks.
- **London Flagship Showroom & Contact**: Direct WhatsApp link (`https://wa.me/...`), interactive contact form, opening hours badge, Google Maps embed.

---

## 📁 Project Structure

```
apex-phones-ecommerce/
├── index.html                      # HTML5 entry with SEO tags & fonts
├── package.json                    # Dependencies & scripts
├── vite.config.js                  # Vite bundler configuration
├── tailwind.config.js              # Tailwind CSS configuration
├── postcss.config.js               # PostCSS plugins
├── vercel.json                     # Vercel SPA routing & cache headers
├── .gitignore                      # Git ignore rules
├── .env.example                    # Environment secrets template
└── src/
    ├── main.jsx                    # React DOM entrypoint
    ├── App.jsx                     # Master router & view switcher
    ├── index.css                   # Custom styles, glassmorphism, scrollbars
    ├── context/
    │   └── ShopContext.jsx         # Global state (Cart, Wishlist, Filters, Orders, Admin)
    ├── data/
    │   ├── shopConfig.js           # ⭐️ CENTRAL SHOP CONFIGURATION (Easy Modification System)
    │   └── products.js             # ⭐️ CENTRAL PRODUCTS & FILTER DATA REPOSITORY
    ├── services/
    │   ├── api.js                  # API & persistence layer (Firebase/Supabase ready)
    │   └── payment.js              # Modular payment gateway abstraction
    └── components/
        ├── Navbar.jsx              # Sticky navigation with live search, wishlist, cart
        ├── Hero.jsx                # Flagship interactive showcase & CTAs
        ├── ProductCard.jsx         # Reusable card with badges, swatches, quick view
        ├── ProductGrid.jsx         # Responsive grid with sorting & active filter chips
        ├── ProductFilters.jsx      # Desktop sidebar & slide-over mobile drawer
        ├── ProductDetails.jsx      # Gallery, specs tabs, swatches, reviews form
        ├── CartDrawer.jsx          # Flyout drawer & standalone cart with coupon support
        ├── Checkout.jsx            # Order validation, delivery choices & payment
        ├── DealsSection.jsx        # Flash sale countdown & discounts
        ├── AccessoriesSection.jsx  # Category pills & accessories catalog
        ├── TrustSection.jsx        # 6 core trust indicators
        ├── ReviewSection.jsx       # Verified customer testimonials
        ├── ContactSection.jsx      # WhatsApp link, showroom details & Google map
        ├── AboutSection.jsx        # Company heritage & 60-point quality check
        ├── AdminDashboard.jsx      # KPI metrics, product manager & order log
        ├── QuickViewModal.jsx      # Rapid lightbox preview modal
        ├── Toast.jsx               # Floating feedback toast notifications
        └── Footer.jsx              # Newsletter, brand directory, security badges
```

---

## 🛠️ Installation & Run Commands

### 1. Install Dependencies
```bash
npm install
```

### 2. Start Development Server
```bash
npm run dev
```
The site runs locally at `http://localhost:3000`.

### 3. Build for Production
```bash
npm run build
```
Creates an optimized production bundle inside the `dist/` folder.

### 4. Preview Production Build Locally
```bash
npm run preview
```

---

## 🌐 Vercel Deployment Instructions

This repository is pre-configured with `vercel.json` for 1-click deployment.

### Method A: Deploy via GitHub / Vercel Web Dashboard (Recommended)
1. Push your repository to GitHub, GitLab, or Bitbucket.
2. Go to [vercel.com](https://vercel.com) and log in.
3. Click **"Add New"** -> **"Project"**.
4. Import your repository.
5. Vercel automatically detects **Vite**:
   - **Framework Preset**: `Vite`
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
6. Click **Deploy**. Your site will be live on a secure HTTPS `.vercel.app` URL within 60 seconds!

### Method B: Deploy via Vercel CLI
```bash
npm install -g vercel
vercel login
vercel
# For production deployment:
vercel --prod
```

---

## ⚙️ Exact Modification Guide (Easy Customization System)

To modify any part of the website, you only need to edit **two centralized files**:

### 1. Changing Shop Information, Phone, Address & Currency
Open `src/data/shopConfig.js`:
```javascript
export const shopConfig = {
  shopName: "YOUR SHOP NAME",             // Changes shop name across nav, hero, footer
  tagline: "Your Custom Tagline",
  contact: {
    phone: "+44 20 7946 0991",            // Updates click-to-call numbers
    whatsapp: "+447946099100",            // Updates WhatsApp links
    whatsappLink: "https://wa.me/447946099100",
    email: "support@yourdomain.com",
    address: {
      street: "Your Address",
      city: "London",
      postcode: "W1D 2DZ"
    }
  },
  currency: {
    symbol: "£",                          // Change to $, €, etc.
    code: "GBP",
    deliveryFreeThreshold: 50.00          // Amount needed for free shipping
  }
};
```

### 2. Adding a New Smartphone or Brand
Open `src/data/products.js` and add an object to the `initialProducts` array:
```javascript
{
  id: "apple-iphone-17-pro",
  sku: "APL-IP17P-256",
  brand: "Apple",
  model: "iPhone 17 Pro",
  category: "smartphones",
  price: 1099,
  originalPrice: 1199,
  discountPercentage: 8,
  stockStatus: "in_stock",
  stockCount: 25,
  rating: 4.9,
  reviewCount: 12,
  images: [
    "https://images.unsplash.com/photo-1695048133142-1a20484d2569?q=80&w=900&auto=format&fit=crop"
  ],
  colors: [
    { name: "Cosmic Titanium", hex: "#3b3d40" }
  ],
  storageOptions: ["256GB", "512GB", "1TB"],
  ramOptions: ["12GB"],
  description: "Next-generation titanium flagship.",
  specifications: {
    display: "6.3\" Super Retina XDR 120Hz",
    processor: "Apple A19 Pro",
    camera: "48MP Triple Fusion"
  }
}
```
*Tip: You can also add, edit, or delete phones live via the Admin Dashboard UI!*

### 3. Changing Promotional Codes & Discounts
In `src/data/shopConfig.js`:
```javascript
flashSale: {
  enabled: true,
  title: "⚡ MEGA FLASH SALE",
  discountCode: "FLASH35",
  discountAmount: "35% OFF",
}
```

---

## 🔒 Payment Gateway Integration (Stripe & PayPal)

The checkout is architected cleanly inside `src/services/payment.js`.

### Connecting Stripe:
1. Install the official Stripe React SDK:
   ```bash
   npm install @stripe/stripe-js
   ```
2. In `.env`, add your publishable key:
   ```env
   VITE_STRIPE_PUBLISHABLE_KEY=pk_live_your_key_here
   ```
3. In `src/services/payment.js`, replace the simulated authorization with:
   ```javascript
   import { loadStripe } from '@stripe/stripe-js';
   const stripe = await loadStripe(import.meta.env.VITE_STRIPE_PUBLISHABLE_KEY);
   const result = await stripe.confirmCardPayment(clientSecret, { payment_method: ... });
   ```

### Connecting PayPal:
1. Install `@paypal/react-paypal-js`:
   ```bash
   npm install @paypal/react-paypal-js
   ```
2. Render `<PayPalButtons />` in `src/components/Checkout.jsx` using `onApprove`.

---

## 🗄️ Database Integration (Firebase & Supabase)

The project includes an abstraction service in `src/services/api.js`.

### Connecting Firebase / Cloud Firestore:
1. Install Firebase:
   ```bash
   npm install firebase
   ```
2. Initialize Firebase in `src/services/firebase.js`:
   ```javascript
   import { initializeApp } from 'firebase/app';
   import { getFirestore } from 'firebase/firestore';
   
   const firebaseConfig = {
     apiKey: import.meta.env.VITE_FIREBASE_API_KEY,
     projectId: import.meta.env.VITE_FIREBASE_PROJECT_ID,
   };
   export const db = getFirestore(initializeApp(firebaseConfig));
   ```
3. In `src/services/api.js`, replace the `localStorage` calls with `getDocs(collection(db, "products"))`.

### Connecting Supabase:
1. Install Supabase:
   ```bash
   npm install @supabase/supabase-js
   ```
2. Query products directly via `supabase.from('products').select('*')`.

---

## 🛡️ Accessibility & Performance

- **Semantic HTML5**: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`
- **ARIA Standards**: Dialog overlays, accessible labels for icon buttons, live alerts
- **Color Contrast**: Compliant with WCAG AA standards
- **Image Optimization**: Native `loading="lazy"` on all offscreen images
- **Zero Heavy Dependencies**: Pure React 18 and Lucide icons without bulky external UI libraries
