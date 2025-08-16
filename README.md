# 🚀 Bunplate - Modern Full-Stack Template

A production-ready template for modern web applications built with Next.js, Bun, and TypeScript. Features authentication, database management, internationalization, payments, and comprehensive CI/CD pipeline.

## ✨ What is Bunplate?

Bunplate is a comprehensive full-stack template that provides everything you need to build modern web applications. It includes:

- **Complete Authentication System** - Kinde Auth with user management
- **Database Management** - PostgreSQL with Prisma ORM  
- **Event Management System** - Registration, payments, and capacity management
- **Payment Processing** - QR codes, bank transfers, and tracking
- **Internationalization** - Multi-language support (EN/CS)
- **Modern UI Components** - Shadcn/ui with Tailwind CSS
- **CI/CD Pipeline** - Automated quality checks and deployment
- **Production Ready** - Security, performance, and monitoring built-in

## 🛠️ Tech Stack

### Frontend
- **Next.js 15+** - React framework with App Router
- **React 18** - Latest React features and hooks
- **TypeScript** - Strict type safety
- **Tailwind CSS** - Utility-first CSS framework
- **Shadcn/ui** - Beautiful, accessible components

### Backend & Database
- **PostgreSQL** - Production-ready database
- **Prisma** - Type-safe ORM with migrations
- **Next.js API Routes** - Serverless endpoints
- **Bun Runtime** - Fast JavaScript runtime

### Authentication & Services
- **Kinde Auth** - Complete authentication solution
- **Resend** - Modern email API service
- **JWT Tokens** - Secure session management

### Development & Quality
- **ESLint & Prettier** - Code quality and formatting
- **Vitest** - Fast unit testing
- **TypeScript Strict Mode** - Maximum type safety
- **GitHub Actions** - Automated CI/CD

## 🚀 Quick Start

### Prerequisites
- **Bun** (>= 1.0.0) - [Download](https://bun.sh)
- **Node.js** (>= 18.0.0) - for compatibility
- **PostgreSQL** database - local or hosted
- **Git** - for version control

### 1. Use This Template

```bash
# Clone the template
git clone <your-template-repo-url> your-app-name
cd your-app-name

# Remove git history and initialize new repo
rm -rf .git
git init
git add .
git commit -m "Initial commit from Bunplate template"
```

### 2. Install Dependencies

```bash
bun install
```

### 3. Environment Setup

```bash
cp .env.example .env.local
# Edit .env.local with your configuration
```

### 4. Database Setup

```bash
bun run db:generate
bun run db:push
bun run db:seed
```

### 5. Start Development

```bash
bun run dev
```

Visit [http://localhost:3000](http://localhost:3000) to see your application.

## 🔧 Configuration

### Required Services

1. **Database** - PostgreSQL (Neon, Supabase, Railway)
2. **Authentication** - [Kinde Auth](https://kinde.com)
3. **Email** - [Resend](https://resend.com)

See [SETUP.md](./SETUP.md) for detailed configuration instructions.

## 📁 Project Structure

```
├── src/
│   ├── app/                    # Next.js app router
│   ├── components/             # React components
│   ├── lib/                    # Utility libraries
│   ├── hooks/                  # React hooks
│   ├── i18n/                   # Internationalization
│   └── types/                  # TypeScript types
├── prisma/                     # Database schema and migrations
├── messages/                   # Translation files
├── scripts/                    # Build and utility scripts
└── docs/                       # Documentation
```

## 🎯 Features

### 🔐 Authentication & Security
- Kinde Auth integration with SSO support
- Role-based access control (USER, ADMIN, MODERATOR)
- Secure session management
- Rate limiting and abuse prevention

### 📊 Event Management
- Create and manage events
- User registration with approval workflows
- Capacity management and waiting lists
- Payment tracking with QR codes
- Email notifications and reminders

### 🌍 Internationalization
- English and Czech language support
- Easy to add more languages
- Dynamic language switching
- Localized email templates

### 💳 Payment System
- Bank account management
- QR code generation for payments
- Payment status tracking
- Multiple payment methods support

### 📧 Communication
- Resend email integration
- Notification templates
- Automated email workflows
- Rate-limited email sending

### 🗄️ Database
- PostgreSQL with Prisma ORM
- Type-safe database operations
- Migration system
- Comprehensive audit logging
- Automated cleanup tasks

## 🚀 Available Commands

### Development
```bash
bun run dev          # Start development server
bun run build        # Build for production
bun run start        # Start production server
```

### Code Quality
```bash
bun run lint         # Run ESLint
bun run format       # Format with Prettier
bun run type-check   # TypeScript checking
bun run test         # Run tests
```

### Database
```bash
bun run db:generate  # Generate Prisma client
bun run db:push      # Push schema changes
bun run db:migrate   # Run migrations
bun run db:seed      # Seed database
bun run db:studio    # Open Prisma Studio
```

### Project Validation
```bash
bun run validate-structure  # Validate project organization
bun run check-all          # Run all quality checks
bun run setup-hooks        # Setup git hooks
```

## 🌐 Deployment

### Vercel (Recommended)
1. Connect your GitHub repository to Vercel
2. Set environment variables in Vercel dashboard
3. Deploy automatically on push to main branch

### Other Platforms
- Railway
- DigitalOcean App Platform
- AWS
- Google Cloud Run

## 🔄 CI/CD Pipeline

Automated quality checks include:
- TypeScript type checking
- ESLint code quality
- Prettier formatting
- Unit tests with coverage
- Database validation
- Security vulnerability scanning

## 📚 Documentation

- **[SETUP.md](./SETUP.md)** - Comprehensive setup guide
- **[Database Schema](./prisma/schema.prisma)** - Data models
- **[Components](./src/components/)** - UI component library

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes with tests
4. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) team for the framework
- [Vercel](https://vercel.com/) for deployment platform
- [Kinde](https://kinde.com/) for authentication
- [Resend](https://resend.com/) for email delivery
- [Prisma](https://prisma.io/) for the ORM
- [Shadcn](https://ui.shadcn.com/) for components

---

Built with ❤️ for modern web development. Happy coding!