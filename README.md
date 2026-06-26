# Quizzter Static Site

This folder contains a simple static website for the app:

- `index.html`: landing page
- `privacy.html`: privacy policy
- `support.html`: support URL page
- `delete-account.html`: account deletion instructions
- `download/index.html`: App Store redirect for `/download`
- `app-ads.txt`: AdMob app authorization file
- `nginx.default.conf`: optional nginx config to redirect `/index.html` to `/`
- `site.css`: shared styling

Deployment notes:

- The support address is `hello@quizzter.com`.
- Host the contents of this folder on your public domain or static hosting provider.
- If you use nginx, you can mount `nginx.default.conf` as `/etc/nginx/conf.d/default.conf` to make `/index.html` redirect to `/` and to reduce stale HTML caching during updates.
- Make sure `app-ads.txt` is served from the root of the exact developer website domain used in App Store Connect, for example `https://quizzter.com/app-ads.txt`.
- Use the hosted URLs in your App Store, Google Play, Apple Sign In, Google Sign-In, and privacy disclosures as needed.

This site is separate from the Flutter `web/` directory so it can be hosted as a lightweight marketing and compliance site without affecting the app's web build.
