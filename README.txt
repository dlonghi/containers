


chown -R root:12000 /opt/eprocv2/web

find /opt/eprocv2/web -type d -exec chmod 750 {} \;

find /opt/eprocv2/web -type f -exec chmod 640 {} \;


find /opt/eprocv2 -type d -exec sudo  /bin/chmod 2755 {} \;

find /opt/eprocv2 -type f -exec sudo  /bin/chmod 0644 {} \;




# Example from redhat okd
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout tls.key -out tls.crt -subj "/CN=localhost" -addext 'subjectAltName = IP:127.0.0.1'

openssl req -x509 -sha512 -nodes -days 3650 -newkey ec -pkeyopt ec_paramgen_curve:secp384r1 -keyout tls.key -out tls.crt -subj "/CN=localhost" -addext "subjectAltName = DNS:localhost, IP:127.0.0.1"

