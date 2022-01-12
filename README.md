# docker-unrar

* provides "unrar" in a container, so it can be run on any host

## how to build

* `docker build -t gunzl1ng3r/unrar:latest .`

## usage

* default behaviour is to run `find . -name '*.rar' -exec unrar e {} \;` in `/files` (find all `.rar` files and unrars them to `/files`)
  * `docker container run -v /opt/storage/05_upload:/files gunzl1ng3r/unrar:latest`
  * `docker container run -d -v /opt/storage/04_done:/files gunzl1ng3r/unrar:latest`

* manual call to `unrar` could look like this
  * `docker run --rm -v /opt/storage/05_upload:/files gunzl1ng3r/unrar:latest unrar e -r MY_FILE.rar`
