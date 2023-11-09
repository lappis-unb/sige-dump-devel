## How to run

### Downloading Dump File for Master

Clone this repository or:

```bash
wget -O dump_db.gz https://gitlab.com/lappis-unb/projects/SMI/sige-dump-devel/-/raw/master/bkp-db-master-21-09-23.json.tar.gz?inline=false
```

### Decompressing Dump File

```bash
tar -xzvf bkp-db-master-21-09-23.json.tar.gz
```

### Loading Dump File

```bash
sudo docker exec -i master-api python3 manage.py loaddata bkp-db-master-21-09-23.json
```

This process can take quite a while.


### Downloading Dump File for Slave

Clone this repository or:

```bash
wget -O dump_db.gz https://gitlab.com/lappis-unb/projects/SMI/sige-dump-devel/-/raw/master/bkp-db-slave-21-09-23.json.tar.gz?inline=false
```

### Decompressing Dump File

```bash
tar -xzvf bkp-db-slave-21-09-23.json.tar.gz
```

### Loading Dump File

```bash
sudo docker exec -i slave-api python3 manage.py loaddata bkp-db-slave-21-09-23.json
```

This process can take quite a while.