# EBFC AI Landing Page — Deploy Result

**Deployed:** February 27, 2026  
**Status:** ✅ LIVE

## URLs

| Type | URL |
|------|-----|
| **Production (Vercel alias)** | https://ebfc-ai-landing.vercel.app |
| **Deploy URL** | https://ebfc-ai-landing-m1gf7k6ux-felipe-ebfcs-projects.vercel.app |
| **Vercel Inspect** | https://vercel.com/felipe-ebfcs-projects/ebfc-ai-landing/2bUy7JNaLGLvLmJVPFXXb9gBxG63 |
| **GitHub Repo** | https://github.com/felipe-ebfc/ebfc-ai |

## Next Steps

1. **Connect Formspree** — Edit `index.html`, find the `handleSubmit` comment, add your Formspree endpoint:
   ```js
   fetch('https://formspree.io/f/YOUR_FORM_ID', { method: 'POST', body: new FormData(form) })
   ```
2. **Point ebfc.ai domain** — Add CNAME `ebfc.ai → cname.vercel-dns.com` in your DNS registrar, then add the domain in Vercel dashboard
3. **Replace launch date** — Update "Early Access March 2026" copy when ready

## Design Notes

- Fonts: Bebas Neue (display) + Space Grotesk (body)
- Colors: #004AAD blue, #D4A827 gold CTA, #0D0D0F dark bg
- Single viewport, no scroll, fade-in animations
- Mobile responsive
- Form captures email client-side, shows success state (backend hookup pending)
