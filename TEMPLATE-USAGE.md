# 🎯 Using the Bunplate Template

This guide will help you quickly customize the Bunplate template for your specific project needs.

## 🚀 Quick Customization Checklist

### 1. Project Identity
- [ ] Update `NEXT_PUBLIC_APP_NAME` in `.env.local`
- [ ] Replace `YourAppName` in `src/components/layout/navigation.tsx`
- [ ] Update translations in `messages/en.json` and `messages/cs.json`
- [ ] Change database name in environment variables

### 2. Branding & UI
- [ ] Replace `favicon.ico` in `public/` directory
- [ ] Update brand colors in `tailwind.config.ts`
- [ ] Customize the landing page in `src/app/[locale]/page.tsx`
- [ ] Update email templates in `prisma/seed.ts`

### 3. Database Customization
- [ ] Update bank account details in `prisma/seed.ts`
- [ ] Modify default roles and permissions as needed
- [ ] Customize event and video categories
- [ ] Update system configuration values

### 4. Authentication Setup
- [ ] Create Kinde Auth account and application
- [ ] Update Kinde configuration in `.env.local`
- [ ] Configure redirect URLs in Kinde dashboard
- [ ] Update auth URLs in `src/lib/auth.ts`

### 5. Email Configuration
- [ ] Sign up for Resend account
- [ ] Add Resend API key to `.env.local`
- [ ] Verify your domain in Resend dashboard
- [ ] Customize email templates and sender information

### 6. Deployment Setup
- [ ] Create new GitHub repository
- [ ] Update CI/CD workflow names if needed
- [ ] Configure Vercel project
- [ ] Set up production environment variables

## 🔧 Common Customizations

### Removing Features You Don't Need

**Remove Video System:**
```bash
# Remove video-related database models from prisma/schema.prisma
# Remove video categories from seed.ts
# Remove video-related permissions from roles
```

**Simplify Payment System:**
```bash
# Remove bank account models if not using bank transfers
# Simplify payment types in the application
# Remove QR code generation if not needed
```

**Remove Internationalization:**
```bash
# Remove unused language files from messages/
# Simplify i18n configuration in src/i18n/
# Remove language switcher component
```

### Adding Your Own Features

**Add New Database Models:**
1. Update `prisma/schema.prisma`
2. Run `bun run db:migrate`
3. Update seed data in `prisma/seed.ts`

**Add New API Endpoints:**
1. Create new files in `src/app/api/`
2. Follow existing patterns for authentication
3. Add appropriate error handling

**Add New UI Components:**
1. Create components in `src/components/`
2. Follow the existing component structure
3. Use Tailwind CSS classes consistently

## 🎨 Styling Guide

### Color Scheme
The template uses a neutral color palette. Update `tailwind.config.ts` to customize:

```typescript
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: {
          // Your primary color palette
        },
        secondary: {
          // Your secondary color palette
        }
      }
    }
  }
}
```

### Component Styling
- Use existing component patterns from `src/components/ui/`
- Follow Shadcn/ui conventions
- Maintain consistent spacing and typography

## 🌍 Internationalization

### Adding New Languages
1. Create new message file in `messages/` (e.g., `messages/fr.json`)
2. Update `src/i18n/routing.ts` to include new locale
3. Add translations for all existing keys
4. Update database seed data for new language

### Customizing Existing Translations
1. Edit `messages/en.json` and `messages/cs.json`
2. Update email templates in seed data
3. Restart development server to see changes

## 🔐 Security Considerations

### Environment Variables
- Never commit `.env` files with real credentials
- Use different API keys for development and production
- Regularly rotate API keys and secrets

### Authentication
- Configure proper redirect URLs in Kinde
- Set up proper CORS settings for production
- Review and customize user roles and permissions

### Database
- Use strong database passwords
- Enable SSL connections in production
- Regularly backup your database

## 📊 Monitoring & Analytics

### Adding Analytics
The template supports several analytics platforms:

```env
# Vercel Analytics
VERCEL_ANALYTICS_ID=your_analytics_id

# PostHog
POSTHOG_KEY=your_posthog_key

# Sentry Error Tracking
SENTRY_DSN=your_sentry_dsn
```

### Performance Monitoring
- Use Vercel's built-in performance monitoring
- Configure error tracking with Sentry
- Monitor database performance with connection pooling

## 🚀 Going to Production

### Pre-Deployment Checklist
- [ ] All environment variables configured
- [ ] Database properly set up and migrated
- [ ] Email service configured and domain verified
- [ ] Authentication redirect URLs updated
- [ ] SSL certificates configured
- [ ] Monitoring and error tracking enabled
- [ ] Backup strategy implemented

### Performance Optimization
- Enable Vercel Edge Functions for API routes
- Use Vercel Image Optimization for images
- Configure proper caching headers
- Optimize database queries and indexing

## 🆘 Getting Help

### Common Issues
1. **Build Errors**: Run `bun run type-check` to identify TypeScript issues
2. **Database Connection**: Verify DATABASE_URL format and credentials
3. **Authentication**: Check Kinde configuration and redirect URLs
4. **Email Issues**: Verify Resend API key and domain verification

### Resources
- [Bunplate Documentation](./README.md)
- [Setup Guide](./SETUP.md)
- [Next.js Documentation](https://nextjs.org/docs)
- [Prisma Documentation](https://www.prisma.io/docs)
- [Kinde Documentation](https://kinde.com/docs)

---

Need more help? Check the issues in the template repository or create a new issue with your specific question.