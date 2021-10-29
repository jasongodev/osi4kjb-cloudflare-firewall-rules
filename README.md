# kajabi-cloudflare-firewall-rules
Cloudflare Firewall rules for Kajabi custom domains for added protection and prevention of excessive 404 responses.
```clojure
(http.host eq "www.jasongo.net")
and (
    (http.request.uri.path contains ".asp") or
    (http.request.uri.path contains ".axd") or
    (http.request.uri.path contains ".dll") or
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
    (http.request.uri.path contains "/wp-login") or
    (http.request.uri.path contains "sellers.json") or
    (http.request.uri.path contains "allowurl.txt")
)
```
Change "www.jasongo.net" to your own Kajabi custom domain.
