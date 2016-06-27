# docker-yourls

**YOURLS** stands for **Your Own URL Shortener**. It is a small set of PHP scripts that will allow you to run your own URL shortening service (a la TinyURL or bitly).

Running your own URL shortener is fun, geeky and useful: you own your data and don't depend on third party services. It's also a great way to add branding to your short URLs, instead of using the same public URL shortener everyone uses.

References:
- http://yourls.org/#About
- https://hub.docker.com/r/fauzanariffin/docker-yourls/

**What is this Docker image all about?**
This Docker image to start a yourls container with Ubuntu, Apache2 and php5.

Quickstart with mysql container

```
docker run --name yourlsmysql -e MYSQL_ROOT_PASSWORD=mysecretpassword -d mysql
docker run --name yourls -d \
-e YOURL_USER='admin' \
-e YOURL_PASSWORD='mysecretpassword' \
-e YOURLS_SITE='http://sh.tld' \
--link yourlsmysql:mysql fauzanariffin/docker-yourls
```
