# Asim Shaikh - AI Entrepreneur Portfolio

A modern, professional landing page showcasing AI innovation and entrepreneurship journey. Built with React, TypeScript, and Express.js featuring a sleek dark theme with 3D effects.

## 🚀 Live Demo

Visit the live portfolio at: [Your deployed URL]

## 📋 About

This portfolio showcases four cutting-edge AI projects:

- **TrustAudit AI** - Revolutionary risk-free auditing for SMEs
- **RecruitWise AI** - Next-gen AI hiring agent  
- **BattWatchdog** - Intelligent energy monitoring system
- **RevuLens Lite** - AI review summarizer for hotels

## 🛠️ Technology Stack

### Frontend
- **React 18** with TypeScript
- **Vite** for fast development and building
- **Tailwind CSS** for styling
- **Framer Motion** for animations
- **Shadcn/ui** components
- **React Query** for state management
- **Wouter** for routing

### Backend
- **Node.js** with Express.js
- **TypeScript** with ES modules
- **Drizzle ORM** for database operations
- **PostgreSQL** with Neon Database
- **Session management** with Express sessions

### Features
- **3D Effects** - Card hover animations and depth
- **Glass Morphism** - Modern UI with backdrop blur
- **Responsive Design** - Mobile-first approach
- **Contact Form** - Functional partnership proposals
- **Professional Animations** - Smooth transitions and interactions

## 🏃‍♂️ Getting Started

### Prerequisites
- Node.js 18+ installed
- PostgreSQL database (or Neon DB)

### Installation

1. Clone the repository
```bash
git clone <repository-url>
cd asim-shaikh-ai-portfolio
```

2. Install dependencies
```bash
npm install
```

3. Set up environment variables
```bash
cp .env.example .env
```

Add your database URL:
```env
DATABASE_URL="your-postgresql-connection-string"
```

4. Run database migrations
```bash
npm run db:push
```

5. Start development server
```bash
npm run dev
```

Visit `http://localhost:5000`

## 📁 Project Structure

```
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   │   ├── sections/   # Page sections (Hero, About, Projects, etc.)
│   │   │   └── ui/         # Shadcn/ui components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── lib/            # Utility functions and configurations
│   │   └── pages/          # Page components
├── server/                 # Backend Express application
│   ├── index.ts           # Server entry point
│   ├── routes.ts          # API routes
│   ├── storage.ts         # Database operations
│   └── vite.ts            # Vite configuration
├── shared/                 # Shared types and schemas
│   └── schema.ts          # Database schemas
└── dist/                  # Production build output
```

## 🚀 Deployment

### Build for Production

```bash
npm run build
```

### Start Production Server

```bash
npm start
```

### Environment Variables

Required for production:
```env
DATABASE_URL="your-postgresql-connection-string"
NODE_ENV="production"
```

## 📧 Contact Form

The contact form allows potential incubators to submit partnership proposals. Data is stored in PostgreSQL and can be retrieved via the admin API.

### API Endpoints

- `POST /api/contact` - Submit contact form
- `GET /api/contact` - Retrieve submissions (admin)

## 🎨 Design Features

### Dark Theme
- Black and charcoal grey color scheme
- High contrast for readability
- Professional appearance

### 3D Effects
- Card hover animations with rotation
- Depth shadows and perspective
- Glass morphism with backdrop blur
- Text shadow effects

### Responsive Design
- Mobile-first approach
- Breakpoint optimization
- Touch-friendly interactions

## 🔧 Development

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run check` - Type checking
- `npm run db:push` - Push database schema

### Code Quality

- TypeScript for type safety
- ESLint for code linting
- Prettier for formatting
- Modular component architecture

## 📄 License

MIT License - feel free to use this code for your own projects.

## 🤝 Contributing

This is a personal portfolio project. For suggestions or improvements, please open an issue.

## 📞 Contact

**Asim Shaikh**
- LinkedIn: [linkedin.com/in/asimshaikh1515](https://linkedin.com/in/asimshaikh1515)
- Email: Available upon request
- Portfolio: [Your deployed URL]

---

*Built with passion for AI innovation and entrepreneurship* 🚀
