# Notes Q&A

An AI-powered app with a login system where Admins manage notes and Users ask questions — answered strictly from those notes.

## Roles

### Admin
- Default login: `admin` / `admin123`
- Paste and save notes (meeting minutes, SOPs, project docs, etc.)
- Enter the Anthropic API key (stored locally in the browser)
- Create and remove user accounts
- View all questions asked by all users

### User
- Accounts created by Admin
- Ask questions — AI answers only from the notes
- View their own question history

## Setup

Single `index.html` file — no build step, no dependencies.

1. Clone the repo
2. Open `index.html` in any browser
3. Sign in as **Admin** (`admin` / `admin123`)
4. Add your Anthropic API key in the Notes tab
5. Paste your notes and save
6. Create user accounts in the Users tab
7. Share the page with your coworkers

## Hosting options

- **GitHub Pages** — push to a repo, enable Pages in Settings → Pages
- **Netlify / Vercel** — drag and drop the folder
- Any static file host

## Notes

- All data (notes, users, history) persists in `localStorage` — stays across refreshes on the same browser
- The API key is stored in `localStorage` — don't share your browser profile
- The model used is `claude-sonnet-4-20250514`
- Change the admin password by editing `nqa_admin_pass` in localStorage or modifying the source
