OpenAI proxy on Cloudflare Worker and Vercel Edge.

If you are close to Hong Kong, it's better to deploy on Vercel. Since Cloudflare will use Hong Kong which is not a supported region for OpenAI API.

## Deployment Options

### Deploy on Vercel:

- Fork this repo
- Add your repo on Vercel

### Deploy on Cloudflare:

```
pnpm i
pnpm run deploy
```

### Deploy on Render:

1. Fork this repo
2. Go to [Render Dashboard](https://dashboard.render.com)
3. Click "New +" → "Web Service"
4. Connect your GitHub repository
5. Configure the following:
   - **Name**: openai-proxy
   - **Runtime**: Node
   - **Build Command**: `npm install && npm run build`
   - **Start Command**: `npm run start`
6. Add environment variables:
   - `OPENAI_API_KEY`: Your OpenAI API key
   - `NODE_ENV`: production
7. Click "Create Web Service"

The application will automatically deploy whenever you push to your repository.
