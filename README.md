# ruuvi-python

https://github.com/ttu/ruuvitag-sensor


lataa 
python -m pip install ruuvitag_sensor

python3 ~/.local/lib/python3.9/site-packages/ruuvitag_sensor -f

aja servisenä
https://gist.github.com/emxsys/a507f3cad928e66f6410e7ac28e2990f

cd /lib/systemd/system/
sudo nano hello.service

sudo systemctl daemon-reload 
sudo chmod 644 /lib/systemd/system/ruuvi.service
sudo systemctl status ruuvi.service 
sudo systemctl start ruuvi.service
sudo systemctl stop ruuvi.service

Check service's log
sudo journalctl -f -u ruuvi.service


https://gist.github.com/emxsys/a507f3cad928e66f6410e7ac28e2990f
