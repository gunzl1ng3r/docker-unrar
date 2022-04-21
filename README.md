# docker-unrar

* provides "unrar" in a container, so it can be run on any host

## how to build

* `docker build -t gunzl1ng3r/unrar:latest .`

## usage

* default behaviour is to run `find . -name '*.rar' -exec unrar e {} \;` in `/files` (find all `.rar` files and unrars them to `/files`)
  * run in foreground
    * `docker container run -v /opt/storage:/files gunzl1ng3r/unrar:latest`
  * run in background
    * `docker container run -d -v /opt/storage:/files gunzl1ng3r/unrar:latest`
