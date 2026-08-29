<div align="center">
  <img src="https://github.com/user-attachments/assets/0078f1c8-4f1c-48d0-8936-8da18fde6960" alt="Imaginify interface" />
</div>

# Imaginify

A full-stack AI image editing app built with Next.js 14. It combines Cloudinary transformations with Clerk authentication, MongoDB persistence and a Stripe-backed credits flow.

## What it does

- restores images and removes backgrounds
- applies generative fill, object removal and object recoloring
- stores transformations in a searchable community gallery
- gives each user a profile and credit balance
- handles authentication with Clerk and checkout with Stripe

## Stack

Next.js · TypeScript · Cloudinary · Clerk · MongoDB · Stripe · Tailwind CSS

## Running locally

You will need Node.js 18.17 or newer and accounts for Clerk, MongoDB, Cloudinary and Stripe.

```powershell
npm ci
Copy-Item .env.example .env.local
npm run dev
```

Fill in `.env.local`, then open [http://localhost:3000](http://localhost:3000).

The application expects these webhook endpoints:

- Clerk: `/api/webhooks/clerk` for user creation, updates and deletion
- Stripe: `/api/webhooks/stripe` for completed checkout sessions

For local webhook testing, expose the development server with a tunnel or use the provider's CLI forwarding tools.

## Acknowledgements

Based on the original [Imaginify reference implementation](https://github.com/adrianhajdin/ai_saas_app).
