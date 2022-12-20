# gen certs with mkcert

1. `mkcert -install`
2. `mksert -cert-file cert.pem -key-file key.pem localhost "domain" "domain2"`
conf/traefik.yml - main config file
conf.d/* - config files for each service. Dynamically loaded by traefik.
