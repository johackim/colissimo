Colissimo
===

Colissimo tracking cli

Install
---

```bash
# Add to .bashrc
colissimo() {
    curl -s -X POST -d "suivi%5Bnumber%5D=$1" http://www.laposte.fr/particulier/outils/suivre-vos-envois | grep -Po '<p class="h5">(.*?)<\/p><\/td>'| sed 's|<[^>]*>||g'
}
```

-- or --

Add `colissimo` to `/usr/local/bin`
