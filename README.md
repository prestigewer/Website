# Prestige Wear (Vite)

## Chalane ka tareeqa
1. Node.js (v18+) install hona chahiye: https://nodejs.org
2. Is folder mein terminal kholo:
   ```
   npm install
   npm run dev
   ```
   Browser mein http://localhost:5173 khul jayega.

## Settings (.env file)
`.env` mein 3 cheezein hain:
- `VITE_SUPABASE_URL`      - Supabase Project URL
- `VITE_SUPABASE_ANON_KEY` - Supabase publishable key
- `VITE_ADMIN_PASSWORD`    - Admin panel ka password

`.env` badalne ke baad `npm run dev` dobara chalao.

## Live karna (deploy)
```
npm run build
```
Isse `dist/` folder banega. Us folder ko Netlify / Vercel / apni hosting par upload karo.

Netlify ya Vercel par project ke Environment Variables mein upar wali 3 values
(`VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY`, `VITE_ADMIN_PASSWORD`) daalna zaroori hai,
kyunki `.env` file upload nahi hoti. Build command: `npm run build`, output folder: `dist`.

## Zaroori note
`VITE_` wali values build ke baad browser code mein aa jati hain, is liye admin password asli security nahi hai.
Public site ke liye Supabase Auth (login) lagana behtar hai.

## Folder
- `index.html`   - page ka HTML
- `src/main.js`  - page ka poora logic + Supabase
- `src/style.css`- design
- `public/`      - images (`public/images`) aur favicon
- `vercel.json`  - Vercel deploy settings
