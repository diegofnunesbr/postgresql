# PostgreSQL

### Instalar o PostgreSQL no Kubernetes:

- `git clone git@github.com:diegofnunesbr/postgresql.git`
- `cd postgresql`
- `helm install --create-namespace postgresql -n postgresql .`

### Configurar o PostgreSQL no arquivo hosts do Windows:

- `sudo tee -a /mnt/c/Windows/System32/drivers/etc/hosts <<< "$(ifconfig eth0 | grep 'inet ' | awk '{print $2}') postgresql.local"`

### Remover o PostgreSQL no Kubernetes:

- `helm uninstall postgresql -n postgresql`
