## How to run

### Downloading Dump File

Clone this repository or:

```bash
wget -O dump_db.gz https://gitlab.com/lappis-unb/projects/SMI/sige-dump-devel/-/raw/master/dump_23-03-2021_22_54_06.gz?inline=false
```

### Decompressing Dump File

```bash
gzip --decompress dumb_db.gz
```

### Loading Dump File

```bash
cat dump_db | sudo docker exec -i master-db psql -U postgres
```