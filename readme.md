### RGB LED Matrix in Python

Prerequisites:
 - Follow the guide [here](https://github.com/hzeller/rpi-rgb-led-matrix/blob/master/bindings/python/README.md) to
   build the python bindings for rpi-rgb-led-matrix
 - Create a `.env` file containing your [mta gtfs](https://new.mta.info/developers) API key as `MTA_KEY={key}` and (on a new line) your [openweathermap key](https://home.openweathermap.org/users/sign_up) as `WEATHER_KEY={key}`
 - run `sudo pip install -r requirements.txt`
 - add `sudo /path/to/start.sh` to your crontab to start it up on boot/schedule

Local Development Tips
- ssh into raspberry pi
- Run `crontab -e`
- Comment out `@reboot cd ~/rgb-matrix && sudo bash ~/rgb-matrix/start.sh`
- Run `sudo reboot now`

Sync changes from local to remote system
- `rsync -avzh -I ~/rgb-matrix <username>@<remote_host>:<destination_directory>`

Run changes instantly
- Run `python3 display.py`
