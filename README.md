# kajabi-cloudflare-firewall-rules
Cloudflare Firewall rules for Kajabi custom domains for added protection and prevention of excessive 404 responses.
```clojure
(http.host eq "www.jasongo.net")
and (
    (http.request.uri.path contains "jasongo.net") or
    (http.request.uri.path contains ".asp") or
    (http.request.uri.path contains ".axd") or
    (http.request.uri.path contains ".dll") or
    (http.request.uri.path contains ".env") or
    (http.request.uri.path contains ".exe") or
    (http.request.uri.path contains ".htaccess") or
    (http.request.uri.path contains ".htpasswd") or
    (http.request.uri.path contains ".jsp") or
    (http.request.uri.path contains ".pdb") or
    (http.request.uri.path contains ".php") or
    (http.request.uri.path contains ".pl") or
    (http.request.uri.path contains ".py") or
    (http.request.uri.path contains "/etc/passwd") or
    (http.request.uri.path contains "/sslvpn_websession") or
    (http.request.uri.path contains "/wp-admin") or
    (http.request.uri.path contains "/wp-content") or
    (http.request.uri.path contains "/wp-includes") or
    (http.request.uri.path contains "/wp-login") or
    (http.request.uri.path contains "_404") or
    (http.request.uri.path contains "sellers.json") or
    (http.request.uri.path contains "allowurl.txt")
)
```
Change YOUR_CUSTOM_DOMAIN_HERE to your own Kajabi custom domain. If it starts with a subdomain (e.g. www, shop, or learn, etc), then include it so it looks like www.yourdomain.com or learn.yourdomain.com. Basically, you use the custom domain configured in your Kajabi account.

Change YOUR_ROOT_CUSTOM_DOMAIN_HERE to the root of your custom domain. For example, if your custom domain is www.yourdomain.com, then root is yourdomain.com only.
