# 🏠 servease-ui

> A modern, full-featured online platform for booking home cleaning and maid services — built with Next.js 15 App Router. Browse service providers, schedule bookings, track status, and manage your home services effortlessly.

![Next.js](https://img.shields.io/badge/Next.js_15-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

---

## 📸 Preview

> _Add a screenshot or screen recording of your app here_
> `![App Preview](./public/preview.png)`

---

## ✨ Features

- 🧹 **Service Catalog** — Browse available cleaning and maid services with pricing
- 📅 **Booking Scheduler** — Pick date, time slot, and service duration
- 👷 **Provider Profiles** — View ratings, reviews, and availability of maids
- 🔔 **Booking Management** — Track upcoming, ongoing, and completed bookings
- 🔐 **Authentication** — Secure login / register for customers and providers
- 💳 **Payment Integration** — Seamless checkout and payment flow
- ⭐ **Ratings & Reviews** — Leave feedback after service completion
- 📱 **Fully Responsive** — Optimized for mobile, tablet, and desktop
- ⚡ **Optimized Performance** — Image optimization via `next/image`, font optimization via `next/font` (Geist)

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | Next.js 15 (App Router) |
| Language | TypeScript |
| Styling | Tailwind CSS |
| Font | Geist (via `next/font`) |
| State Management | Zustand / Context API |
| HTTP Client | Axios / Fetch API |
| Auth | NextAuth v5 |
| Deployment | Vercel |

---

## 📁 Folder Structure

```
servease-ui/
├── app/
│   ├── (auth)/
│   │   ├── login/
│   │   │   └── page.tsx
│   │   └── register/
│   │       └── page.tsx
│   ├── (dashboard)/
│   │   ├── bookings/
│   │   │   ├── [id]/
│   │   │   │   └── page.tsx      # Booking detail & tracking
│   │   │   └── page.tsx          # All bookings list
│   │   └── profile/
│   │       └── page.tsx
│   ├── services/
│   │   ├── [id]/
│   │   │   └── page.tsx          # Service detail + booking CTA
│   │   └── page.tsx              # Service catalog listing
│   ├── providers/
│   │   ├── [id]/
│   │   │   └── page.tsx          # Provider profile + reviews
│   │   └── page.tsx              # Browse providers
│   ├── checkout/
│   │   └── page.tsx              # Booking summary + payment
│   ├── layout.tsx                # Root layout
│   └── page.tsx                  # Landing / home page
├── components/
│   ├── ui/                       # Reusable UI primitives (Button, Modal, Badge)
│   ├── booking/                  # BookingCard, BookingForm, DateTimePicker
│   ├── service/                  # ServiceCard, ServiceFilter, PriceTag
│   ├── provider/                 # ProviderCard, RatingStars, ReviewList
│   └── layout/                   # Navbar, Footer, Sidebar
├── lib/
│   ├── api.ts                    # API client / fetchers
│   └── utils.ts                  # Utility functions
├── store/                        # Zustand store (booking, auth, filters)
├── types/                        # Global TypeScript interfaces
├── public/                       # Static assets
└── ...config files
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js `>= 18.x`
- npm / yarn / pnpm / bun

### Installation

```bash
# Clone the repository
git clone https://github.com/chaudhary-rishabh/servease-ui.git
cd servease-ui

# Install dependencies
pnpm install
```

### Environment Variables

Create a `.env.local` file in the root:

```env
NEXT_PUBLIC_API_URL=http://localhost:5000/api
NEXT_PUBLIC_APP_URL=http://localhost:3000
NEXTAUTH_SECRET=your_nextauth_secret
NEXTAUTH_URL=http://localhost:3000
```

> ⚠️ Never commit `.env.local` to version control.

### Run Development Server

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🔗 Backend

This frontend is paired with **[servease-server](https://github.com/chaudhary-rishabh/servease-server)** — a REST API built with Node.js / Express handling bookings, providers, auth, scheduling, and payments.

---

## 🗺️ App Flow

```
Landing Page
    │
    ├──> Browse Services ──> Service Detail ──> Select Provider
    │                                                  │
    │                                           Schedule Booking
    │                                                  │
    │                                           Checkout + Payment
    │                                                  │
    └──> Dashboard ──> Booking Tracker ──> Rate & Review
```

---

## 📦 Scripts

| Command | Description |
|---|---|
| `pnpm dev` | Start development server |
| `pnpm build` | Create production build |
| `pnpm start` | Start production server |
| `pnpm lint` | Run ESLint |
| `pnpm type-check` | Run TypeScript compiler check |

---

## 🌐 Deployment

Optimized for **[Vercel](https://vercel.com)** — connect your GitHub repo for automatic CI/CD on every push to `main`.

```bash
pnpm build
```

---

## 🤝 Contributing

1. Fork the repo
2. Create your feature branch: `git checkout -b feat/your-feature`
3. Commit your changes: `git commit -m "feat: add your feature"`
4. Push to the branch: `git push origin feat/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

<p align="center">Built with ❤️ by <a href="https://github.com/chaudhary-rishabh">Rishabh Chaudhary</a></p>
