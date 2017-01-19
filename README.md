Colissimo
===

> A simple CLI tool to track your packages

Install
---

```bash
# Add to .bashrc
colissimo() {
  curl -s -X POST -d "suivi%5Bnumber%5D=$1" https://www.laposte.fr/particulier/outils/suivre-vos-envois | \
  grep -Po '<p class="h5">(.*?)<\/p><\/td>' | \
  sed 's|<[^>]*>||g'
}
```

-- or --

Add `colissimo` to `/usr/local/bin`

Usage
---

`collisimo <track_number>`

License
---

MIT

**Free Software, Hell Yeah!**
