# luce-on-grimoirelab

THis repo contains small notes for setting-up/tips and related usefull info about GrimoireLab (https://github.com/chaoss/grimoirelab)

# Installation

The grimoirelab installation need some steps. 


I just reordered most of them here.

___
0) grimoirelab install

```bash
sudo pip3 install grimoirelab
pip3 install sortinghat
```
___
1) elasticsearch install

Make sure you have elastisearch installed and running for your distro.

___
2) Database install and sortinghat.

Download and install `mysql` and `mariadb` database.

Once you have the database service running and enabled (which can be remotely or on your localhost), 
create a special user which grimoirelab will use, take inspiration from doc. https://dev.mysql.com/doc/refman/8.0/en/adding-users.html

In the above example i just give the user all rights to database. In production you might chose more restrictive rights.

```bash
mysql --user=root mysql
CREATE USER 'sortinghat2'@'localhost' IDENTIFIED BY 'YOUR_PASSWORD';
GRANT USAGE ON *.* TO sortinghat2@localhost IDENTIFIED BY 'YOUR_PASSWORD';
```

In this example i'm creating settingup sortinhat2.

grimoirelab2 is just a name for the database you can change it
```bash
sortinghat -u sortinghat2 -p YOUR_PASSWORD init grimoirelab2
```

Well done!

___
3) kibiter installation.

download latest release
`https://github.com/chaoss/grimoirelab-kibiter/releases`

___
4) Now use sirmordred

You need to fill project.json and menu.json file. ( WIP finish this.)

```bash
sirmordred -c example.cfg 
```


___
For full doc look here: https://chaoss.github.io/grimoirelab-tutorial/basics/supporting.html and other pages there.
