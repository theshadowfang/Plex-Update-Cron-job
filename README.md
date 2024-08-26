**Plex Update**

jls

jexec # csh

pkg install ca_root_nss
pkg install wget
pkg install perl5

mkdir /usr/local/PMS_Updater
cd /usr/local/PMS_Updater

fetch -o PMS_Updater.sh https://raw.githubusercontent.com/theshadowfang/PLEX-PMS_Updater/main/PMS_Updater.sh

chmod 755 PMS_Updater.sh

./PMS_Updater.sh -vv -a

**Cron Jobs
/usr/local/bin/iocage exec plexmediaserver-plexpass /bin/sh /usr/local/PMS_Updater/PMS_Updater.sh -v -a
