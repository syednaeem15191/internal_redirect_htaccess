# internal_redirect_htaccess

put these lines in your document root directory ".htaccess" files to redirect

`
    RewriteEngine on
    RewriteCond %{HTTP_HOST} ^example.com$ [NC,OR]
    RewriteCond %{HTTP_HOST} ^www.example.com$
    RewriteCond %{REQUEST_URI} !master/project/public/
    RewriteRule (.*) /master/project/public/$1 [L]
`
