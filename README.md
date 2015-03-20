## Building phantomjs 2 for heroku

Important thing to make sure is to build binaries in virtual machine that's running exact same OS as heroku. As of
writing of this README it's Ubuntu 14.04. I've used server edition just in case, but I'm pretty sure it would work
with desktop edition too.

Phantomjs recommends downloading source code in zip package rather than taking source from git, but at least for me
compiling from zip didn't work and I had to use git source.

For up to date build instructions check http://phantomjs.org/build.html

Build instructions used:

```
sudo apt-get install build-essential g++ flex bison gperf ruby perl \
  libsqlite3-dev libfontconfig1-dev libicu-dev libfreetype6 libssl-dev \
  libpng-dev libjpeg-dev ttf-mscorefonts-installer

git clone git://github.com/ariya/phantomjs.git
cd phantomjs
git checkout 2.0
./build.sh
```

It takes really long time when running on VM, but it should eventually build.

## License

This code is released under the [MIT License](http://www.opensource.org/licenses/MIT).
