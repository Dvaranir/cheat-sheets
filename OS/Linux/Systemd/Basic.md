## Start service
```bash
sudo systemctl start SERVICE_NAME.service
```

## Check status service
```bash
sudo systemctl status SERVICE_NAME.service
```

## Check stop service
```bash
sudo systemctl stop SERVICE_NAME.service
```

## Adding new service
```bash
sudo nano /etc/systemd/system/NEW_SERVICE_NAME.service
```
### Inside new service
```
[Unit]  
Description=My test service  
After=multi-user.target[Service]  
Type=simple  
Restart=always  
ExecStart=/usr/bin/python3 /home/<username>/PROGRAM.py[Install]  
WantedBy=multi-user.target
```
### Next step
```bash
sudo systemctl daemon-reload
```
```bash
sudo systemctl enable SERVICE_NAME.service
```
```bash
sudo systemctl start SERVICE_NAME.service
```

## Check if service is running by script
```bash
systemctl is-active --quiet service && DO SOMETHING
```