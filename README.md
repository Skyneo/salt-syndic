========
SaltStack Syndic container
========

OS platforms
======================
CentOS 7

``Starting container``
------------------

docker run -d --restart=unless-stopped -e SALT_SYNDIC_ID='SlaveMaster' -e SALT_ENV='base' -e SALT_MASTER_PUBLISH='4505' -e SALT_MASTER_PORT='4506' -e SALT_MOM_IP='megamaster.host.local' -p 4506:4506 -p 4505:4505 -v /opt/salt/base:/opt/salt/base--name salt-common smonko/syndic

``Arguments``
------------------
SALT_MASTER_PUBLISH - publish port for salt master
SALT_MASTER_PORT - port for minion auth and respond
SALT_SYNDIC_ID - id which will show syndic on master of masters server
SALT_MOM_IP - IP or hostname of master of masters
SALT_ENV - enviromet to be created inside container
