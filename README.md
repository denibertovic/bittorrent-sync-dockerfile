# Bittorrent Sync Dockerfile

Clone the repo:

    git clone https://github.com/denibertovic/bittorrent-sync-dockerfile

Build

    docker build -t btsync .

Make sync folder on your desktop:
    
    mkdir -p /home/myuser/btsync/.sync

Copy example config (you need to at least modify the auth cretentials):
    
    cp btsync.conf.example /home/myuser/btsync/

Run:

    docker run -p 8888:8888 -p 55555:55555 -v /home/myuser/btsync:/btsync btsync

And visit the web interface on http://YourIP:8888/
