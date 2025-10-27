# Deployment Guide

## Vercel Deployment

### Step 1: Prepare Your Repository

Ensure your code is pushed to GitHub:

\`\`\`bash
git add .
git commit -m "Ready for deployment"
git push origin main
\`\`\`

### Step 2: Connect to Vercel

1. Go to [vercel.com](https://vercel.com)
2. Click "New Project"
3. Select your GitHub repository
4. Click "Import"

### Step 3: Configure Environment Variables

In the Vercel dashboard:

1. Go to Settings → Environment Variables
2. Add the following variables:

\`\`\`
OPENAI_API_KEY = sk-your-actual-key-here
NODE_ENV = production
\`\`\`

### Step 4: Deploy

1. Click "Deploy"
2. Wait for the build to complete
3. Your app will be live at `https://your-project.vercel.app`

## Environment Variables

### Required for Production

- **OPENAI_API_KEY**: Your OpenAI API key
  - Get it from [platform.openai.com/api-keys](https://platform.openai.com/api-keys)
  - Keep this secret - never commit it to version control

### Optional

- **NODE_ENV**: Set to `production` (Vercel does this automatically)

## Security Checklist

- [ ] OpenAI API key is set in Vercel environment variables
- [ ] API key is NOT in `.env.local` or committed to git
- [ ] `.env.local` is in `.gitignore`
- [ ] HTTPS is enabled (automatic on Vercel)
- [ ] Security headers are configured in `next.config.mjs`

## Monitoring

After deployment:

1. Check Vercel Analytics dashboard
2. Monitor API usage in OpenAI dashboard
3. Set up alerts for rate limiting
4. Review error logs in Vercel

## Troubleshooting

### Build Fails

- Check Node.js version compatibility
- Verify all environment variables are set
- Check build logs in Vercel dashboard

### API Errors

- Verify OpenAI API key is correct
- Check API usage limits in OpenAI dashboard
- Review rate limiting configuration

### Performance Issues

- Check Vercel Analytics
- Optimize images and assets
- Review database queries (if using database)

## Scaling

For production use:

1. **Database**: Migrate from localStorage to Supabase/Neon
2. **Authentication**: Implement OAuth with NextAuth.js
3. **Caching**: Add Redis for session management
4. **Monitoring**: Set up error tracking with Sentry
5. **Analytics**: Add analytics with Vercel Analytics

## Support

For deployment issues:
- Check [Vercel Documentation](https://vercel.com/docs)
- Review [Next.js Deployment Guide](https://nextjs.org/docs/deployment)
- Contact Vercel support
