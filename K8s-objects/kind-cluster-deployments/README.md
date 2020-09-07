```bash
curl -v -HHost:kind-clstr.com \
--resolve "kind-clstr.com:80:127.0.0.1" \
"kind-clstr.com/foo"

curl -v -HHost:kind-clstr.com \
--resolve "kind-clstr.com:80:127.0.0.1" \
"kind-clstr.com/bar"
```