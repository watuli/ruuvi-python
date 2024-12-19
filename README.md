# ruuvi-python

https://github.com/ttu/ruuvitag-sensor

HUOM jos feilaa noiden jälkeen aja

sudo rm /usr/lib/python3.*/EXTERNALLY-MANAGED

lataa 

python3 -m pip install ruuvitag_sensor

sudo pip3 install ruuvitag_sensor

sudo pip3 install influxdb

python3.11 ~/.local/lib/python3.11/site-packages/ruuvitag_sensor -f

####################
aja servisenä
https://gist.github.com/emxsys/a507f3cad928e66f6410e7ac28e2990f

cd /lib/systemd/system/
sudo nano ruuvi.service

[Unit]
Description=RUUVI TAG python
After=multi-user.target

[Service]
Type=simple
ExecStart=/usr/bin/python3 /home/mice/scripts/ruuvi-python/post_to_influxdb.py
Restart=on-abort

[Install]
WantedBy=multi-user.target

======================================

sudo systemctl daemon-reload 
sudo chmod 644 /lib/systemd/system/ruuvi.service
sudo systemctl status ruuvi.service 
sudo systemctl start ruuvi.service
sudo systemctl stop ruuvi.service

Check service's log
sudo journalctl -f -u ruuvi.service


https://gist.github.com/emxsys/a507f3cad928e66f6410e7ac28e2990f
