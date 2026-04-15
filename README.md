# Despliegue

Vamos a utilizar terraform.
Lo primero es habilitar los proveedores, desde la carpeta donde se encuentra terraform:

```
cd iac
```

```
terraform init
```

---

## Crear y seleccionar ambientes

Crear ambiente local:

```
terraform workspace new localhost
```

Crear ambiente dev:

```
terraform workspace new dev
```

Seleccionar ambiente:

```
terraform workspace select localhost
```

o

```
terraform workspace select dev
```

---

## Variables por entorno

terraform.tfvars:

```
web_port = {
    localhost = 4001
    dev       = 5001
}

api_port = {
    localhost = 4002
    dev       = 5002
}

db_port = {
    localhost = 4003
    dev       = 5003
}
```

---

## Despliegue

```
terraform apply
```

---

## Destruir infraestructura

```
terraform destroy
```

---

## Puertos por entorno

LOCALHOST:

* Web: 4001
* API: 4002
* DB: 4003

DEV:

* Web: 5001
* API: 5002
* DB: 5003



