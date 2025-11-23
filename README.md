# JokePan - Digital Product Marketplace Platform

A modern, full-featured marketplace platform for selling digital products with built-in bulk buyer contact system.

## Features

✨ **Product Management**
- Browse premium digital products
- Advanced filtering and search
- Product details with ratings and reviews
- Category-based organization

💼 **Bulk Buyer Platform**
- Dedicated bulk inquiry form with volume-based pricing tiers
- Automatic bulk price calculation
- Company information management
- Dedicated support for bulk orders

🛒 **E-commerce Features**
- Product catalog with responsive design
- Shopping cart integration
- Instant digital downloads
- Lifetime access to purchased products

🎨 **Modern Design**
- Clean, professional UI
- Fully responsive (mobile, tablet, desktop)
- Fast performance with Next.js
- Accessibility-first approach

## Tech Stack

- **Framework**: Next.js 15+ with React 19
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: shadcn/ui & Lucide Icons
- **Node Package Manager**: npm

## Getting Started

### Prerequisites
- Node.js 18+ (recommended 20+)
- npm, yarn, pnpm, or bun

### Installation & Development

1. Navigate to the project directory:
```bash
cd jokepan
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Build for Production

```bash
npm run build
npm start
```

### Linting

Check code quality:
```bash
npm run lint
```

## Key Pages

- **Homepage** (`/`): Hero section, featured products, why choose us, categories, bulk order CTA
- **Products** (`/products`): Full catalog with filters, search, and sorting
- **Product Details** (`/products/[id]`): Detailed view with reviews, bulk pricing, related products
- **Bulk Inquiry** (`/bulk-inquiry`): Contact form for volume purchases with automatic pricing suggestions
- **About** (`/about`): Company info, values, statistics, feature highlights

## Project Structure

```
src/
├── app/
│   ├── page.tsx              # Homepage
│   ├── products/
│   │   ├── page.tsx          # Product catalog
│   │   └── [id]/
│   │       └── page.tsx      # Product details
│   ├── bulk-inquiry/
│   │   └── page.tsx          # Bulk buyer form
│   ├── about/
│   │   └── page.tsx          # About page
│   └── layout.tsx            # Root layout
├── components/
│   ├── Header.tsx            # Navigation header
│   ├── Footer.tsx            # Footer component
│   └── ProductCard.tsx       # Product card component
├── data/
│   └── products.ts           # Mock product data
└── types/
    └── index.ts              # TypeScript types
```

## Bulk Pricing System

Products support tiered bulk pricing:
```typescript
bulkPrices: [
  { quantity: 10, discountPercentage: 10 },
  { quantity: 25, discountPercentage: 20 },
  { quantity: 50, discountPercentage: 30 },
]
```

The system automatically calculates discounted prices based on quantity ordered.

## Mock Data

The platform includes 6 sample products across 4 categories:
- **Design**: Design System, Figma Kit
- **Code**: React Component Library
- **Templates**: E-commerce Template, Documentation Template
- **Assets**: UI Icon Pack

Replace with your actual product data by modifying `src/data/products.ts`.

## Customization

### Change Brand Colors
Edit Tailwind configuration in `tailwind.config.js` or use inline color classes.

### Update Product Data
Edit `src/data/products.ts` with your product information.

### Modify Bulk Pricing
Update bulk price tiers in product definitions.

### Add New Pages
Create new folders in `src/app/` following Next.js conventions.

## Integration Points

### Ready for Backend Integration:
1. **Product API**: Replace mock data with API calls to your backend
2. **Bulk Inquiry**: Integrate with email/database service (currently simulates submission)
3. **Authentication**: Add NextAuth.js or similar for user accounts
4. **Payments**: Integrate Stripe, PayPal, or other payment processors
5. **Search**: Connect to Elasticsearch for advanced search

### Environment Variables
Create a `.env.local` file:
```env
NEXT_PUBLIC_API_URL=your_api_url
DATABASE_URL=your_database_url
EMAIL_SERVICE_KEY=your_email_service_key
```

## Performance Features

- ⚡ Static site generation for fast load times
- 🔄 Incremental Static Regeneration (ISR) ready
- 📦 Optimized bundle with tree-shaking
- 🖼️ Image optimization with Next.js Image component

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Troubleshooting

### Port 3000 already in use
```bash
npm run dev -- -p 3001
```

### Build errors
Clear cache and reinstall:
```bash
rm -r .next node_modules
npm install
npm run build
```

### Styling issues
Ensure Tailwind CSS is properly installed:
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

## Deployment

### Deploy to Vercel (Recommended)

1. Push code to GitHub
2. Import project in [Vercel Dashboard](https://vercel.com)
3. Vercel automatically deploys on push

### Deploy to Other Platforms

- **Netlify**: Connect GitHub repo, set build command to `npm run build`
- **AWS Amplify**: Use AWS Amplify with Next.js support
- **Self-hosted**: Use Docker or standard Node.js hosting

## Environment Setup for Deployment

```env
# Production
NEXT_PUBLIC_API_URL=https://your-production-api.com
NODE_ENV=production
```

## Support & Contact

### Get in Touch
- **Email**: info@jokepan.live
- **Phone**: +32 466 382 790
- **Business Email**: wholesale@jokepan.com
- **Live Chat**: Available 9 AM - 6 PM EST (Monday-Friday)

### Social & Web
- **Website**: https://jokepan.live (Production)
- **GitHub**: https://github.com/jokepan/jokepan
- **Local Dev**: http://localhost:3000
- **Business Hours**: Monday - Friday, 9:00 AM - 6:00 PM EST

### Website & Design Services
We offer professional website design and e-commerce solutions. Contact us at:
- **Phone**: +32 466 382 790
- **Email**: info@jokepan.live
- **Services**: Custom web design, marketplace development, Alibaba integration

### For Bulk Orders
Contact our wholesale team:
- **Phone**: +32 466 382 790
- **Email**: wholesale@jokepan.com
- **Form**: Use the `/bulk-inquiry` page on the platform

### Quick Support
Use the in-app ChatBot (bottom-right corner) for:
- Product information
- Pricing inquiries
- Alibaba integration help
- Shipping details
- Payment methods

---

**Version**: 1.0.0
**Last Updated**: November 23, 2025
**Brand**: JokePan B2B Wholesale Marketplace
**Contact**: +32 466 382 790 | info@jokepan.live
**Website**: https://jokepan.live
**Tech Stack**: Next.js 16, TypeScript, Tailwind CSS, React 19
