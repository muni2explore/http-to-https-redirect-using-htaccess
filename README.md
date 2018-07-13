# HTTP to HTTPS Redirect using htaccess

Create .htaccess file in your public_html folder if not exists. Add following conditions in it to redirect from http to https.
```htaccess
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

