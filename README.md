# BackupDell1
```
fdisk -l
mkdir -p /media/USB
mount -t auto /dev/sdd /media/USB
mount  /dev/sdd1 /media/USB
cd /media/USB
ls
mkdir dell1
cd dell1
 h=`pwd`
echo $h

rsync -Prltvc /home/ekozik /media/USB/dell1/home
rsync -Prltvc /home/lizkozik /media/USB/dell1/home
rsync -Prltvc /home/family /media/USB/dell1/home
rsync -Prltvc /home/nf /media/USB/dell1/home
rsync -Prltvc /home/jkozik --exclude={"*.vdi","*.iso"} /media/USB/dell1/home
cd /backup
cd mysql
ls
cp alldatabases.20220921.05.sql.gz /media/USB/dell1/home/
rsync -Prltvc /etc /media/USB/dell1/etc
df -h /media/USB

umount /media/USB
lsof
lsof /media/USB
914  echo $PID

lsof /media/USB
umount /media/USB
```

