# Domain Select

*Apache 2* configuration file with accompanying *Bash* script for redirection of web visitors based on the value of the `Accept-Language` header.

Copy the Bash script `domain-select` to `/usr/local/bin` and make it executable:

```bash
cp domain-select /usr/local/bin
chmod +x /usr/local/bin/domain-select
```

Edit the language-domain map in the `domain-select` file:

```php
static $lang_site_map = [
  'en' => 'https://www.example.com/',
  'sv' => 'https://www.exempel.se/',
];
```


Include the `domain-select.conf` in your virtual host configuration (not in a `<Directory>…</Directory>`),

Finally, restart Apache server.

```bash
service apache2 restart
```
