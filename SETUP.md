# Chotu Garment: setup
1. Upload the whole `site` folder to Netlify / Vercel / GitHub Pages (index.html = public site, admin/ = admin panel).
2. Supabase > Authentication > Users > Add user (your email + a strong password).
3. Supabase > SQL Editor, run (use your email):
   insert into public.admin_users(user_id) select id from auth.users where email = 'YOUR-EMAIL';
4. Supabase > Authentication > Sign In / Providers: turn OFF "Allow new users to sign up".
5. Open /admin/login and sign in.
