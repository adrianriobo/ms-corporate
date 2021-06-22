# ms-corporate
IaC to create a corporate environment microsoft based

## Container

Build
```bash
podman build -t terraform:1.0.0 .
```

Run
```bash
podman run -it --rm \
        --workdir=/provision \
        -v $PWD:/provision:Z \
        -e OS_AUTH_URL=XXX \
        -e OS_USERNAME=XXX \
        -e OS_TENANT_ID=XXX \
        -e OS_PROJECT_DOMAIN_ID=XXX \
        -e OS_PASSWORD=XXX \
        localhost/terraform:1.0.0
```
