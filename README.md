# Nexus Installtion Steps

```
 #  apt update
 #  set-hostname nexus
 #  apt install openjdk-8-jre-headless
 #  useradd -m -s /bin/bash nexus
 $  curl -L -O https://sonatype-download.global.ssl.fastly.net/repository/downloads-prod-group/3/nexus-3.30.1-01-unix.tar.gz
 $  tar -xf nexus-3.30.1-01-unix.tar.gz
 $  rm -rf nexus-3.30.1-01-unix.tar.gz
 $  mv nexus-3.30.1-01/ nexus
 $  cd nexus && cd bin 
 $  ./nexus start 
 ```
 start service with systemd
 ```
 #  ln -s /home/nexus/nexus/bin/nexus /etc/init.d/nexus 
 #  echo "run_as_user=nexus" >/home/nexus/nexus/bin/nexus.rc
 #  systemctl enable nexus
 #  systemctl start nexus
 #  systemctl status nexus
 ```
