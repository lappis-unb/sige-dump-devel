## How to run

### Downloading Dump File for Master

Clone this repository or:

```bash
wget -O dump_db_part_aa.gz "https://gitlab.com/lappis-unb/projects/SMI/sige-dump-devel/-/raw/master/bkp-db-master-21-09-23.json.tar.gz_part_{aa,ab}?inline=false"
```

### Decompressing Dump File

```bash
cat bkp-db-master-21-09-23.json.tar.gz_part_a* | tar -xzvf -
```

### Loading Dump File

```bash
sudo docker exec -i master-api python3 manage.py loaddata bkp-db-master-21-09-23.json
```

This process can take quite a while.


### Downloading Dump File for Slave

Clone this repository or:

```bash
wget -O dump_db_part_aa.gz "https://gitlab.com/lappis-unb/projects/SMI/sige-dump-devel/-/raw/master/bkp-db-slave-21-09-23.json.tar.gz_part_{aa,ab}?inline=false"
```

### Decompressing Dump File

```bash
cat bkp-db-slave-21-09-23.json.tar.gz_part_a* | tar -xzvf -
```

### Loading Dump File

```bash
sudo docker exec -i slave-api python3 manage.py loaddata bkp-db-slave-21-09-23.json
```

This process can take quite a while.