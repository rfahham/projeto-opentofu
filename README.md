# Migrando do Terraform para OpenToFu

The open source infrastructure as code tool.

## Repositório
https://opentofu.org/

## Principal alteração

O Registry, onde se armazena os providers
  No terraform registry.terraform.io
  No Opentofu registry.opentofu.org

## Instalação
https://opentofu.org/docs/intro/install/

```bash
mkdir opentofu
cd opentofu
curl --proto '=https' --tlsv1.2 -fsSL https://get.opentofu.org/install-opentofu.sh -o install-opentofu.sh
chmod +x install-opentofu.sh
./install-opentofu.sh --install-method standalone
tofu --version
OpenTofu v1.7.1
on linux_amd64
```


