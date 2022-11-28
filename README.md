
# R-N301 custom component for homeassistant

Place files in '${HOMEASSISTANTCONFIG}/custom_components/rn301/'

Restart HA before configuring devices. Other wise you will get an error message like "Platform error media_player.rn301 - Integration 'rn301' not found".



##Development

Component development requires libraries for editor and place where new features can be run.

###Libraries

Prepare ubuntu

    sudo apt-get install autoconf libssl-dev libxml2-dev libxslt1-dev libjpeg-dev libffi-dev libudev-dev zlib1g-dev pkg-config
    sudo apt-get install -y libavformat-dev libavcodec-dev libavdevice-dev libavutil-dev libswscale-dev libavresample-dev libavfilter-dev
    sudo apt-get install python3-venv

Install venv - virtual environments for project and place for home assistant libs

    python3.7 -m venv venv
    source venv/bin/activate.fish

Install home assistant libraries - local installation not need special permission and use `sudo`

    python3 -m pip install homeassistant
    
    
###Docker
    
Install home assistant in docker (https://www.home-assistant.io/docs/installation/docker/)

    docker run --init -d --name="home-assistant-rn301" -v /PATH_TO_YOUR_CONFIG:/config --net=host homeassistant/home-assistant:stable
