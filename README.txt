


chown -R root:12000 /opt/eprocv2/web

find /opt/eprocv2/web -type d -exec chmod 750 {} \;

find /opt/eprocv2/web -type f -exec chmod 640 {} \;


find /opt/eprocv2 -type d -exec sudo  /bin/chmod 2755 {} \;

find /opt/eprocv2 -type f -exec sudo  /bin/chmod 0644 {} \;

