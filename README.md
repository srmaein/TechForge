# ⚡ TechVerdict — Technology Review Blog

> A professional, objective, and detailed technology review platform built for tech enthusiasts and informed consumers.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Visual Strategy](#-visual-strategy)
- [Color Scheme](#-color-scheme)
- [Typography](#-typography)
- [Page Structure](#-page-structure)
- [Component Architecture](#-component-architecture)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [File Structure](#-file-structure)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Data Schema](#-data-schema)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🔍 Overview

**TechVerdict** is a modern technology review blog designed with an editorial-first approach. It provides in-depth product reviews, side-by-side comparisons, and data-driven purchasing suggestions. Every design decision prioritizes **clarity, objectivity, and depth** — ensuring readers can make informed decisions.

### Target Audience

| Audience | Description |
|---|---|
| **Tech Enthusiasts** | Crave detailed parameters and teardown insights |
| **Conscious Consumers** | Need clear pros/cons and comparison tools |
| **Gadget Geeks** | Love unboxing experiences and benchmark data |

### Core Principles

| Principle | Description |
|---|---|
| **Professional** | Expert-level analysis with verified data |
| **Objective** | Unbiased reviews with transparent methodology |
| **Detailed** | No surface-level takes — deep dives into every aspect |
| **Practical** | Real-world usage scenarios and actionable suggestions |

---

## 🎨 Visual Strategy

### Imagery

| Type | Usage |
|---|---|
| Product Photos | Solid-color background (white/dark gray) product shots |
| Disassembly Diagrams | Labeled teardown visuals with component callouts |
| Comparison Tables | Side-by-side parameter grids with highlight differentials |
| Parameter Lists | Structured spec sheets in tabular format |
| Data Visualizations | Bar charts, radar charts, and score breakdowns |

### Composition

- **Contrastive Layout** — Split-screen comparisons (Product A vs Product B)
- **Data-First Design** — Charts and tables take visual priority over decorative elements
- **Modular Cards** — Review previews in consistent, scannable card grids
- **Grid Background** — Subtle grid patterns to reinforce the tech aesthetic

### Photography Guidelines

```
✅ DO:
  - Solid white or dark gray backgrounds
  - Multiple angle shots (front, back, side, ports)
  - Scale references (hand/coin beside product)
  - Consistent lighting — soft, diffused, no harsh shadows

❌ DON'T:
  - Lifestyle/ambient shots as primary images
  - Overly processed or filtered photos
  - Cluttered backgrounds
  - Watermarked images
```

---

## 🎨 Color Scheme

### Primary Palette

| Color | Hex | RGB | Usage |
|---|---|---|---|
| **Dark Gray** | `#1A1A2E` | `26, 26, 46` | Primary background, headers, nav |
| **Deep Gray** | `#16213E` | `22, 33, 62` | Card backgrounds, secondary sections |
| **Tech Blue** | `#0F8FFF` | `15, 143, 255` | Primary accent, links, buttons, charts |
| **Pure White** | `#FFFFFF` | `255, 255, 255` | Text on dark, section backgrounds |
| **Light Gray** | `#F0F0F5` | `240, 240, 245` | Alternate row backgrounds, borders |

### Semantic Colors

| Color | Hex | Usage |
|---|---|---|
| **Fluorescent Red** | `#FF2D55` | Disadvantages, warnings, negative highlights |
| **Success Green** | `#30D158` | Advantages, positive ratings, recommendations |
| **Amber** | `#FFD60A` | Neutral/mixed verdicts, medium ratings |
| **Muted Gray** | `#8E8E93` | Secondary text, disabled states, placeholders |

### Background Patterns

```css
/* Solid Dark */
.bg-solid {
  background-color: #1A1A2E;
}

/* Grid Pattern */
.bg-grid {
  background-color: #1A1A2E;
  background-image:
    linear-gradient(rgba(15, 143, 255, 0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(15, 143, 255, 0.03) 1px, transparent 1px);
  background-size: 40px 40px;
}

/* Dot Pattern */
.bg-dots {
  background-color: #1A1A2E;
  background-image: radial-gradient(rgba(15, 143, 255, 0.08) 1px, transparent 1px);
  background-size: 24px 24px;
}
```

### Color Usage Rules

```
■ Tech Blue     (#0F8FFF) → Advantages, links, CTAs, chart highlights, scores
■ Fluor. Red    (#FF2D55) → ONLY for disadvantages, cons, critical warnings
■ Green         (#30D158) → Positive indicators, "Recommended" badges
■ White         (#FFFFFF) → Primary text on dark backgrounds
■ Dark Gray     (#1A1A2E) → Primary background, creates depth and focus
```

---

## 🔤 Typography

### Font Stack

| Role | Font | Fallback | Weight |
|---|---|---|---|
| **Headings** | `Space Grotesk` | `system-ui, sans-serif` | 700, 800 |
| **Body** | `Inter` | `system-ui, sans-serif` | 400, 500 |
| **Data/Code** | `JetBrains Mono` | `monospace` | 400, 500 |
| **Labels** | `Inter` | `system-ui, sans-serif` | 600 |

### Type Scale

```css
:root {
  /* Headings */
  --text-h1: 3rem;          /* 48px — Hero titles */
  --text-h2: 2.25rem;       /* 36px — Section titles */
  --text-h3: 1.5rem;        /* 24px — Card titles */
  --text-h4: 1.25rem;       /* 20px — Subsections */

  /* Body */
  --text-body: 1rem;        /* 16px — Paragraph text */
  --text-body-lg: 1.125rem; /* 18px — Lead paragraphs */
  --text-small: 0.875rem;   /* 14px — Metadata, captions */
  --text-xs: 0.75rem;       /* 12px — Labels, tags */

  /* Line Heights */
  --leading-tight: 1.25;
  --leading-normal: 1.6;
  --leading-relaxed: 1.75;
}
```

### Text Styling Rules

- **Ratings** — Bold, Tech Blue color; exceptional scores get a subtle glow
- **Parameters** — Monospace font within structured tables
- **Pros** — Prefixed with `+` icon in green
- **Cons** — Prefixed with `-` icon in Fluorescent Red
- **Verdicts** — Bold, larger font, color-coded badge (Recommended / Value / Avoid)

---

## 📄 Page Structure

### 1. Homepage — Hero

```
┌─────────────────────────────────────────────────────────────┐
│  [LOGO]    Reviews  Compare  Brands  About    [🔍] [Subscribe] │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌──────────────────┐  ┌──────────────────────────────────┐ │
│  │  Blogger Photo   │  │  LATEST REVIEW                   │ │
│  │                  │  │  ━━━━━━━━━━━━━━━━━━━━            │ │
│  │  @TechVerdict    │  │  Samsung Galaxy S25 Ultra        │ │
│  │  1.2K Reviews    │  │  ★★★★☆  8.7/10                  │ │
│  │  Since 2019      │  │                                  │ │
│  │  [Subscribe]     │  │  [Read Full Review →]            │ │
│  └──────────────────┘  └──────────────────────────────────┘ │
│                                                             │
│  ┌──────┐  ┌──────┐  ┌──────┐  ┌────────┐                  │
│  │ 152  │  │  47  │  │  23  │  │  8.4   │                  │
│  │Reviews│  │Brands│  │Comps │  │AvgScore│                  │
│  └──────┘  └──────┘  └──────┘  └────────┘                  │
└─────────────────────────────────────────────────────────────┘
```

### 2. Review List Page

```
┌─────────────────────────────────────────────────────────────┐
│  BROWSE REVIEWS                                             │
├──────────┬──────────────────────────────────────────────────┤
│ FILTERS  │  REVIEW CARDS                                    │
│          │                                                  │
│ Category │  ┌────────────────────────────────────────────┐  │
│ ○ Phones │  │ [IMG]  Pixel 9 Pro    ★★★★☆  8.5/10      │  │
│ ○ Laptops│  │        Snapdragon X    $999    [Compare]   │  │
│ ○ Audio  │  └────────────────────────────────────────────┘  │
│ ○ Tablets│  ┌────────────────────────────────────────────┐  │
│          │  │ [IMG]  MacBook Pro M4  ★★★★★  9.2/10      │  │
│ Brand    │  │        Apple M4        $1,599  [Compare]   │  │
│ ○ Apple  │  └────────────────────────────────────────────┘  │
│ ○ Samsung│  ┌────────────────────────────────────────────┐  │
│ ○ Google │  │ [IMG]  Sony WH-1000XM5 ★★★★☆  8.8/10     │  │
│ ○ Sony   │  │        Bluetooth 5.3   $348    [Compare]   │  │
│          │  └────────────────────────────────────────────┘  │
│ Price    │                                                  │
│ ○ <$500  │  [Load More ↓]                                  │
│ ○ $500-1K│                                                  │
│ ○ $1K+   │                                                  │
└──────────┴──────────────────────────────────────────────────┘
```

### 3. Review Detail Page

```
┌─────────────────────────────────────────────────────────────┐
│  Samsung Galaxy S25 Ultra — Full Review                     │
│  ★★★★☆ 8.7/10  |  Reviewed: Jan 15, 2025                  │
├─────────────────────────────────────────────────────────────┤
│  [Unboxing] [Experience] [Parameters] [±Pros/Cons] [Buy]    │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ▸ UNBOXING                                                 │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐       │
│  │  Front   │ │  Back    │ │  Box     │ │ Contents │       │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘       │
│                                                             │
│  ▸ EXPERIENCE SCORES                                        │
│  Performance  ████████████████░░  9.0                       │
│  Camera       █████████████████░  9.2                       │
│  Battery      ██████████████░░░░  8.0                       │
│  Display      █████████████████░  9.4                       │
│  Build        ████████████████░░  8.8                       │
│                                                             │
│  ▸ PARAMETER TABLE                                          │
│  ┌────────────┬──────────────┬──────────────┐               │
│  │ Parameter  │ S25 Ultra    │ iPhone 16 Pro│               │
│  ├────────────┼──────────────┼──────────────┤               │
│  │ Chipset    │ SD 8 Elite   │ A18 Pro      │               │
│  │ RAM        │ 12GB         │ 8GB          │               │
│  │ Battery    │ 5000mAh      │ 3582mAh      │               │
│  └────────────┴──────────────┴──────────────┘               │
│                                                             │
│  ▸ PROS & CONS                                              │
│  ┌─────────────────────┬─────────────────────────┐          │
│  │ ✅ ADVANTAGES       │ ❌ DISADVANTAGES         │          │
│  │ + Best Android cam  │ - Heavy (218g)           │          │
│  │ + S Pen included    │ - Slow charging vs China │          │
│  │ + 7yr updates       │ - Expensive ($1,299+)    │          │
│  └─────────────────────┴─────────────────────────┘          │
│                                                             │
│  ▸ PURCHASING SUGGESTIONS                                   │
│  🏆 RECOMMENDED FOR: Power users, photographers             │
│  ⚠️  AVOID IF: Budget < $1,000 or prefer compact phones     │
│  Best Price: $1,249 at Amazon  [Buy →]                      │
│                                                             │
│  ▸ COMMUNITY                                                │
│  Was this helpful?  [👍 142] [👎 8]                         │
│  [Poll] Samsung vs Apple?  Samsung 64%  Apple 36%           │
│  💬 Comments (23)                                           │
└─────────────────────────────────────────────────────────────┘
```

### 4. Comparison Tool

```
┌─────────────────────────────────────────────────────────────┐
│  ⚖️ COMPARE PRODUCTS                                        │
├─────────────────────────────────────────────────────────────┤
│  [+ Add Product]    [+ Add Product]    [+ Add Product]      │
│                                                             │
│  ┌─────────────────┬─────────────┬───────────┬──────────┐   │
│  │                 │ Pixel 9 Pro │ S25 Ultra │ iP16 Pro │   │
│  ├─────────────────┼─────────────┼───────────┼──────────┤   │
│  │ Overall Score   │    8.5      │   8.7     │   9.0    │   │
│  │ Price           │    $999     │  $1,299   │  $1,199  │   │
│  │ Performance     │    8.8      │   9.0     │   9.1    │   │
│  │ Camera          │    9.0      │   9.2     │   8.9    │   │
│  │ Battery         │    8.2      │   8.0     │   8.5    │   │
│  │ Value for Money │    9.1      │   7.5     │   7.8    │   │
│  └─────────────────┴─────────────┴───────────┴──────────┘   │
│                                                             │
│  📊 RADAR CHART         💰 PRICE COMPARISON                 │
│      Performance        Pixel 9 Pro   ████████  $999        │
│         /\              iPhone 16 Pro ██████████ $1,199      │
│  Camera   Display       S25 Ultra     ████████████ $1,299   │
│         \/                                                   │
└─────────────────────────────────────────────────────────────┘
```

---

## 🧱 Component Architecture

```
src/components/
├── layout/
│   ├── Navbar              # Logo, nav links, search, subscribe
│   ├── Footer              # Links, newsletter, social
│   ├── Sidebar             # Filters for review list
│   └── Container           # Max-width wrapper
│
├── hero/
│   ├── BloggerProfile      # Photo, name, stats, subscribe CTA
│   ├── LatestReview        # Featured review card
│   └── StatsBar            # Review count, brands, avg score
│
├── reviews/
│   ├── ReviewCard          # Thumbnail, title, score, price
│   ├── ReviewList          # Filterable grid of ReviewCards
│   ├── ReviewDetail        # Full review page container
│   ├── UnboxingGallery     # Image gallery with captions
│   ├── ExperienceSection   # Score bars and writeup
│   ├── ParameterTable      # Structured spec comparison
│   ├── ProsCons            # Split advantages/disadvantages
│   ├── PurchaseSuggestion  # Recommendations + buy links
│   └── VerdictBadge        # Recommended / Value / Avoid
│
├── compare/
│   ├── CompareSelector     # Add/remove products
│   ├── CompareTable        # Side-by-side parameter table
│   ├── CompareChart        # Radar/bar comparison chart
│   └── PriceComparison     # Visual price bar chart
│
├── interactive/
│   ├── VotingWidget        # Helpful/not helpful buttons
│   ├── PollWidget          # Binary/multi-option polls
│   ├── CommentSection      # Threaded comments
│   ├── CommentForm         # Add comment with validation
│   ├── SubscribeForm       # Email subscription
│   └── RatingDisplay       # Star/number rating component
│
├── dataviz/
│   ├── ScoreBar            # Horizontal score bar
│   ├── RadarChart          # Multi-axis comparison chart
│   ├── BarChart            # Category comparison
│   └── Sparkline           # Price history mini-chart
│
└── ui/
    ├── Button              # Primary, secondary, ghost variants
    ├── Badge               # Category, score, verdict badges
    ├── TabNav              # Review section navigation
    ├── SearchBar           # Product search with autocomplete
    ├── FilterGroup         # Category/brand/price filters
    ├── Toast               # Notifications
    └── Modal               # Image lightbox, confirmations
```

---

## ⚙️ Features

### Content
- [x] In-depth product reviews with structured sections
- [x] Unboxing photo galleries with annotated callouts
- [x] Real-world experience scoring across multiple categories
- [x] Detailed parameter/spec tables
- [x] Clear advantages and disadvantages split-view
- [x] Context-aware purchasing suggestions
- [x] Disassembly/teardown diagrams

### Comparison
- [x] Side-by-side comparison (up to 4 products)
- [x] Visual radar chart for multi-axis scoring
- [x] Price comparison bar chart
- [x] Rating comparison with winner highlighting
- [x] Auto-suggest products to compare

### Interactive
- [x] "Was this review helpful?" voting
- [x] Community polls on product preferences
- [x] Threaded comment system
- [x] Email subscription for new reviews
- [x] Search with auto-complete
- [x] Filter by category, brand, and price range

### Data Visualization
- [x] Horizontal score bars per category
- [x] Radar charts for multi-product comparison
- [x] Price history sparklines
- [x] Rating distribution breakdown
- [x] Benchmark comparison charts

---

## 🛠 Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| **Framework** | Next.js 14+ (App Router) | SSR, routing, API routes |
| **Language** | TypeScript | Type safety |
| **Styling** | Tailwind CSS | Utility-first styling |
| **Charts** | Recharts / Chart.js | Data visualization |
| **Database** | PostgreSQL + Prisma | Reviews, users, comments |
| **Auth** | NextAuth.js | User authentication |
| **Search** | Fuse.js / Meilisearch | Product search |
| **CMS** | MDX / Sanity | Review content authoring |
| **Deployment** | Vercel | Hosting & CI/CD |
| **Analytics** | Vercel Analytics | Privacy-first analytics |
| **Email** | Resend | Subscription notifications |

---

## 📁 File Structure

```
techverdict/
├── public/
│   ├── images/
│   │   ├── products/            # Product photography
│   │   ├── blogger/             # Profile images
│   │   └── brands/              # Brand logos
│   ├── icons/
│   └── fonts/
│
├── src/
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx             # Home / Hero
│   │   ├── reviews/
│   │   │   ├── page.tsx         # Review list
│   │   │   └── [slug]/page.tsx  # Review detail
│   │   ├── compare/page.tsx
│   │   ├── brands/[brand]/page.tsx
│   │   └── api/
│   │       ├── reviews/
│   │       ├── comments/
│   │       ├── vote/
│   │       └── subscribe/
│   │
│   ├── components/              # See Component Architecture
│   │
│   ├── lib/
│   │   ├── db.ts                # Prisma client
│   │   ├── utils.ts             # Helper functions
│   │   ├── scoring.ts           # Score calculation logic
│   │   └── constants.ts         # Colors, breakpoints, etc.
│   │
│   ├── data/
│   │   ├── reviews/             # MDX review files
│   │   └── products/            # Product spec JSON files
│   │
│   ├── styles/globals.css
│   └── types/
│       ├── review.ts
│       ├── product.ts
│       └── comment.ts
│
├── prisma/
│   ├── schema.prisma
│   └── seed.ts
│
├── tailwind.config.ts
├── next.config.mjs
├── tsconfig.json
└── package.json
```

---

## 🚀 Installation

### Prerequisites

- Node.js 18+
- PostgreSQL 14+ (or Docker)
- npm / yarn / pnpm

### Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/techverdict.git
cd techverdict

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local

# Set up the database
npx prisma migrate dev
npx prisma db seed

# Start the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Environment Variables

```env
# .env.local

# Database
DATABASE_URL="postgresql://user:password@localhost:5432/techverdict"

# Authentication
NEXTAUTH_SECRET="your-secret-key"
NEXTAUTH_URL="http://localhost:3000"

# Email (Resend)
RESEND_API_KEY="re_xxxxxxxxxxxx"

# Optional: Search
MEILISEARCH_HOST="http://localhost:7700"
MEILISEARCH_KEY="your-master-key"
```

---

## ⚙️ Configuration

### Tailwind Config

```typescript
// tailwind.config.ts
import type { Config } from 'tailwindcss'

const config: Config = {
  content: ['./src/**/*.{js,ts,jsx,tsx,mdx}'],
  theme: {
    extend: {
      colors: {
        'dark-gray':        '#1A1A2E',
        'deep-gray':        '#16213E',
        'tech-blue':        '#0F8FFF',
        'fluorescent-red':  '#FF2D55',
        'success-green':    '#30D158',
        'amber':            '#FFD60A',
        'muted-gray':       '#8E8E93',
        'surface-light':    '#F0F0F5',
      },
      fontFamily: {
        heading: ['Space Grotesk', 'system-ui', 'sans-serif'],
        body:    ['Inter', 'system-ui', 'sans-serif'],
        mono:    ['JetBrains Mono', 'monospace'],
      },
      backgroundImage: {
        'grid-pattern':
          'linear-gradient(rgba(15, 143, 255, 0.03) 1px, transparent 1px), ' +
          'linear-gradient(90deg, rgba(15, 143, 255, 0.03) 1px, transparent 1px)',
      },
      backgroundSize: {
        'grid': '40px 40px',
      },
    },
  },
  plugins: [],
}

export default config
```

---

## 📊 Data Schema

### Review

```typescript
interface Review {
  id: string
  slug: string
  title: string
  productName: string
  brand: string
  category: 'phones' | 'laptops' | 'audio' | 'wearables' | 'tablets' | 'cameras' | 'other'
  price: number
  currency: string
  dateReviewed: Date

  overallScore: number   // 0–10
  scores: {
    performance: number
    camera: number
    battery: number
    display: number
    build: number
    value: number
    software: number
  }

  unboxing: {
    images: { src: string; alt: string; caption: string }[]
    summary: string
  }
  experience: {
    sections: { title: string; content: string; score: number }[]
  }
  parameters: {
    group: string
    specs: { label: string; value: string }[]
  }[]

  pros: string[]
  cons: string[]
  purchaseSuggestions: {
    recommended: string[]
    alternatives: string[]
    bestPrice: number
    bestPriceUrl: string
    bestPriceStore: string
  }

  verdict: 'recommended' | 'value' | 'average' | 'avoid'
  relatedProducts: string[]   // slugs
  tags: string[]
  featured: boolean
  published: boolean
}
```

### Product

```typescript
interface Product {
  id: string
  name: string
  slug: string
  brand: string
  category: string
  price: number
  releaseDate: Date
  images: {
    front: string
    back: string
    side: string
    box: string
  }
  specGroups: {
    groupName: string
    specs: { key: string; value: string }[]
  }[]
}
```

### Comment

```typescript
interface Comment {
  id: string
  reviewId: string
  userId: string
  userName: string
  userAvatar: string
  content: string
  parentId: string | null   // threaded replies
  createdAt: Date
  upvotes: number
}
```

---

## 🗺 Roadmap

### Phase 1 — Foundation ✅
- [x] Project setup with Next.js + TypeScript + Tailwind
- [x] Color system and typography
- [x] Homepage hero with blogger profile
- [x] Review list with filtering

### Phase 2 — Core Content ✅
- [x] Review detail page with tabbed navigation
- [x] Unboxing gallery component
- [x] Experience scoring visualization
- [x] Parameter table component
- [x] Pros/Cons split view

### Phase 3 — Comparison 🔄
- [ ] Side-by-side comparison tool
- [ ] Radar chart component
- [ ] Price comparison visualization
- [ ] Auto-suggest product matching

### Phase 4 — Interactive 🔄
- [ ] Comment system with threading
- [ ] Voting widget
- [ ] Community polls
- [ ] Email subscription flow

### Phase 5 — Polish 📋
- [ ] SEO optimization
- [ ] Performance audit
- [ ] Accessibility audit (WCAG 2.1 AA)
- [ ] Dark/light mode toggle
- [ ] RSS feed
- [ ] PWA support

### Phase 6 — Advanced 📋
- [ ] Price tracking history
- [ ] AI-powered review summaries
- [ ] Video review embedding
- [ ] User-submitted reviews
- [ ] Affiliate link management

---

## 🤝 Contributing

1. **Fork** the repository
2. Create a feature branch — `git checkout -b feature/amazing-feature`
3. Commit your changes — `git commit -m 'Add amazing feature'`
4. Push to the branch — `git push origin feature/amazing-feature`
5. Open a **Pull Request**

### Coding Standards

- TypeScript strict mode enabled
- ESLint + Prettier for code formatting
- All components must be properly typed
- New components need corresponding documentation
- Follow the color scheme strictly — no arbitrary colors

### Design Standards

- Use only the defined color palette
- Fluorescent Red is **only** for disadvantages/warnings
- All product images must have solid backgrounds
- Charts use Tech Blue primary with semantic accent colors
- Maintain grid/solid background patterns for tech aesthetic

---

## 📝 Content Guidelines

### Writing Reviews

1. **Be objective** — State facts first, opinions clearly labeled
2. **Be thorough** — Cover all scoring categories
3. **Be practical** — Real-world usage over synthetic benchmarks
4. **Be fair** — Acknowledge strengths even in mediocre products
5. **Be clear** — Technical terms explained for a general audience

### Scoring Methodology

| Score | Meaning |
|---|---|
| **10** | Exceptional, best-in-class |
| **9.0+** | Excellent, highly recommended |
| **8.0+** | Very good, recommended with minor caveats |
| **7.0+** | Good, solid choice with notable trade-offs |
| **6.0+** | Average, consider alternatives |
| **5.0+** | Below average, significant drawbacks |
| **< 5.0** | Not recommended |

### Image Requirements

| Image Type | Resolution | Format | Background |
|---|---|---|---|
| Product Front | 1200×1200px | WebP | White `#FFFFFF` |
| Product Back | 1200×1200px | WebP | White `#FFFFFF` |
| Unboxing | 1600×900px | WebP | Natural |
| Teardown | 1600×900px | WebP | Dark `#1A1A2E` |
| Comparison | 1600×900px | WebP | White/Dark |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

- **Email** — smeainrahman@gmail.com
- **GitHub** — [github.com/techverdict](https://github.com/srmaein)

---

<p align="center">
  <strong>TechVerdict</strong> — Professional. Objective. Detailed. Practical.<br/>
  Built with ⚡ for tech enthusiasts who demand the truth.
</p>
