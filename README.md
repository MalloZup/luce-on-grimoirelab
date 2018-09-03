# luce-on-grimoirelab

THis repo contains small notes for setting-up/tips and related usefull info about GrimoireLab (https://github.com/chaoss/grimoirelab)

# one shot install 

```bash
sudo pip3 install grimoirelab
pip3 install sortinghat
```

Make sure you have elastisearch installed and running for your distro.



# single components install


# 1. Perceval

First you want to get the data. Use perceval for it.

https://github.com/chaoss/grimoirelab-perceval


```bash
pip3 install perceval
```

Try if it works:
``` perceval github elastic logstash --from-date '2016-01-01'```

# 2  other steps needed

```
pip3 install grimoire-elk
pip3 install grimoire-kidash
```
