# Chotu Garment: deploy + admin setup

## Deploy on Netlify (plain static site, no build step)
The folder you publish MUST contain index.html, admin/, netlify.toml and _redirects directly inside it.
- Drag-and-drop: Netlify > Add new site > Deploy manually > drop the unzipped `chotu-garment-site` folder (the one that holds index.html and admin/).
- Git: build command empty, publish directory "." (netlify.toml already says this).
After deploying, open https://YOUR-SITE/admin/login/ . If it shows 404, the admin folder was not uploaded.

## First admin (only once)
1. Supabase > Authentication > Users > Add user (email + strong password).
2. SQL Editor: insert into public.admin_users(user_id) select id from auth.users where email = 'YOUR-EMAIL';
3. Authentication > Sign In / Providers: turn OFF "Allow new users to sign up".
4. Sign in at /admin/login/
