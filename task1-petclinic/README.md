# TASK:

Create a docker-compose file with the following containers:
alpine, mysql, jenkins ,petclinic

- mysql should store all information inside of the volume, so after recreation data should persist
- communication between mysql,jenkins,petclinic should be non-accesible from outside
- on alpine (using dockerfile) should be installed nginx and reverse-proxy to jenkins to be accesible
- petclinic should connect to mysql and be accessible trough nginx from alpine container

- create dockerfile for builing mysql, jenkins and keep size as small ass possible
- use jenkins to build and deploy petclinic (you can use alpine container or up new one)