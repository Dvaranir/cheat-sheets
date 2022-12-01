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
After=multi-user.target
[Service]
Type=simple
Restart=always
ExecStart=/home/telegram-bot/letit-telegram-bot/venv/bin/python3 /home/telegram-bot/letit-telegram-bot/Index.py
[Install]
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
systemctl is-active --quiet SERVICE && DO_SOMETHING_IF_RUNNING || DO_SOMETHING_IF_NOT_RUNNING
```
#### Example
```bash
systemctl is-active --quiet telegram-bot.service && echo "Bot is running" || systemctl start telegram-bot.service
```
## Show logs
```bash
journalctl -u SERVICE_NAME.service
```