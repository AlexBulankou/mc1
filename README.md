To solve the problem with `Error while loading shared libraries: libz.so.1: failed to map segment from shared object: Operation not permitted`:

```
mkdir $HOME/tmp
export TMPDIR=$HOME/tmp
docker-compose --version
```

To update to the new image:
```
docker-compose pull
docker-compose up --force-recreate --build -d
```

Use this to as reference: https://minecraft.fandom.com/wiki/Server.properties


### Changing  permissions to this dir
sudo find ./mc1 -type d -exec chgrp evanpermissions {} \;
sudo find ./mc1 -type d -exec chmod 775 {} \;
sudo find ./mc1 -type f -exec chgrp evanpermissions {} \;
sudo find ./mc1 -type f -exec chmod 775 {} \;

### copy from host example
scp /Users/alexbu/Downloads/KyrenLifesteal2-v1.0.jar alexb@bulankou.com:/home/alexb/src/github.com/ab/mc1/data/plugins

