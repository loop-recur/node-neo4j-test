node-neo4j-test
===============

So you're making a node app with neo4j. Now you need to unit test
all your beautiful cypher queries. Mocking the REST API calls won't
verify the logic of your queries. Making REST calls against your dev
database makes test isolation difficult.

Neo4j-test makes testing your app against a real neo4j a little easier.
It uses [loop-recur/neo4j-test-server](https://github.com/loop-recur/neo4j-test-server)
and provides scripts to bring up (and eventually, take down) your test
REST server.

Installation and usage
----------------------

    npm install [-g] neo4j-test
    [./node_modules/neo4j-test/bin/]neo4j-test [-qr]

Options:
* `-q`, `--quiet`: Supress `neo4j start` output.
* `-r`, `--repeatable`: Exit with success if a test neo4j server is already running. The default `neo4j start` script exits with code `2` if a server is running on its port.

Future
------

Add libraries for starting and stopping the neo test server programatically.
