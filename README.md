# Heroku buildpack: Vert.x

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for [Vert.x](http://vertx.io/) apps. Example application [vertx-sample](https://github.com/mthenw/vertx-sample).

Currently it uses following versions:

* JDK **1.8**
* Vert.x **3.0.0-milestone3**

## Usage

This buildpack assumes that there are at least two files in repository:

* ```mod.json``` - used to determine if this is vert.x project
* ```server.js``` - by default file that will be launched (of course this can be overrided by Procfile)

Example usage:

    $ ls
    mod.json server.js

    $ heroku create --buildpack https://github.com/mthenw/heroku-buildpack-vertx.git#v3

    $ git push heroku master

    -----> Fetching custom git buildpack... done
    -----> Vert.x app detected

    -----> Installing OpenJDK7u2..... done
    -----> Installing Vert.x..... done

    -----> Launching... done

## License

MIT
