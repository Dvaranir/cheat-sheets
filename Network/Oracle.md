# Open ports in Oracle cloud

## Create an Ingress Rule in Oracle Cloud vps's dashboard/Networking/Virtual Cloud Networks

## Next install and start
    sudo apt-get install firewalld
    sudo systemctl enable firewalld
    sudo systemctl start firewalld

## Then open port, in example 80 port will be open
    sudo firewall-cmd --zone=public --add-port=80/tcp --permanent  #  or --add-service=http 
    sudo firewall-cmd --reload

## Verify
    sudo firewall-cmd --list-all

## Run python server to test
    python3 -m http.server 80
    