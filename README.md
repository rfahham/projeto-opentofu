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

## Executando o terraform

```bash
terraform init

terraform plan

terraform apply
```

### OBS

Será criada as pastas .terraform/providers/registry.terraform.io

## Verificando criação do pods

```bash
 kubectl get pods                      
NAME                                  READY   STATUS    RESTARTS   AGE
nginx-deployment-2-79cbb6b976-dpbcm   1/1     Running   0          71s
nginx-deployment-2-79cbb6b976-mx5ql   1/1     Running   0          71s
```


## Verificando o deploy

```bash
kubectl get deploy          
NAME                 READY   UP-TO-DATE   AVAILABLE   AGE
nginx-deployment     2/2     2            2           47s

```

## Executando a conversão

```bash
tofu init

tofu plan

tofu apply
```

### OBS

Será criada as pastas .terraform/providers/registry.opentofu.org

