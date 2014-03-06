# Heroku buildpack: Vert.x

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for [Vert.X](http://vertx.io/) apps.

Currently it uses following versions:

* JDK **1.7**
* vert.x **2.0.2-final**

## Usage

This buildpack assumes that there are at least two files in repository:

* ```mod.json``` - used to determine if this is vert.x project
* ```server.js``` - by default file that will be launched (of course this can be overrided by Procfile)

Example usage:

    $ ls
    mod.json server.js

    $ heroku create --stack cedar --buildpack https://github.com/mthenw/heroku-buildpack-vertx.git

    $ git push heroku master

    -----> Heroku receiving push
    -----> Fetching custom build pack... done
    -----> Vert.x app detected
    -----> Installing Vert.x..... done

This buildpack is based on [tomaslin/heroku-buildpack-vertx-jdk7](https://github.com/tomaslin/heroku-buildpack-vertx-jdk7).

## License

MIT