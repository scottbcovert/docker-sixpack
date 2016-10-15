# Dockerized Sixpack server, for a/b-testing

The Docker container contains sixpack and sixpack-web server environment.

## Simple Usage

If you just run sixpack with docker, you can use trusted builds registered [Docker index][di],

    docker-compose up -d

## Deploying

* Run `docker build . -t sixpack-server`

## Running

Another example of running sixpack is:

* Run `docker run -d -t --name sixpack-server -p 5000:5000 -p 5001:5001 sixpack-server`

## Dokku Usage

If using Dokku you will need to set up port mapping between your Dokku host and the sixpack-server container directly from your Dokku host's terminal:

* Run `dokku config:set [App Name] DOKKU_PROXY_PORT_MAP="http:80:5001 http:8080:5001 https:443:5001 https:5000:5000 https:8443:5001"`

## Contributing

Once you've made your great commits:

1. [Fork][fk] docker-sixpack
2. Create your feature branch (``git checkout -b my-new-feature``)
3. Write tests
4. Run tests with ``rake test``
5. Commit your changes (``git commit -am 'Added some feature'``)
6. Push to the branch (``git push origin my-new-feature``)
7. Create new pull request
8. That's it!

## Resources

Sixpack is a language-agnostic a/b-testing framework.

* [Introduction page](http://sixpack.seatgeek.com)
* [Sixpack repo](https://github.com/seatgeek/sixpack)


[fk]: http://help.github.com/forking/
[di]: https://index.docker.io/u/scottbcovert/sixpack/