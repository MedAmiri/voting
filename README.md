Example Voting App
==================

Architecture
-----

* A Python webapp which lets you vote between two options
* A Redis queue which collects new votes
* A Java worker which consumes votes and stores them in…
* A Postgres database backed by a Docker volume
* A Node.js webapp which shows the results of the voting in real time

Running
-------

Since this app makes use of Compose's experimental networking support, it must be started with:

    $ cd vote-apps/
    $ docker-compose --x-networking up -d

The app will be running on port 5000 on your Docker host, and the results will be on port 5001.
Fork from https://github.com/bfirsh/example-voting-app.git
