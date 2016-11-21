# devopsdays-warsaw-2016-minimesos

## Contents

Slides and demo for the [minimesos talk at DevOpsDays Warsaw 2016](https://www.nluug.nl/activiteiten/events/nj16/abstracts/ab11.html)

## Demo

### The environment

Show that no containers are running

```
docker ps
```

### Starting the cluster

```
$ minimesos --debug up
```

* Check the state

```
$ minimesos state | less
```

* Check the processes

```
$ minimesos ps
```

### Exploring the master UI

* Check out the running tasks: Elasticsearch and Weave Scope.
* Check out the resources.

### Exploring Mesos Elasticsearch

* Check out the *Frameworks* tab. Elasticsearch should be running. From here you can check out the tasks.
* Check the 'tasks' menu.
* Check the Elasticsearch endpoint.
* Index a tweet.

```
$ curl -XPUT -d@tweet.json IP:PORT/twitter/tweet/1
```

* Perform a search.
* Scale up.
* Show the `_nodes` endpoint.

### Exploring the Mesos Elasticsearch Sandbox 

* Show the downloaded files and logs

### Exploring Weave Scope

* Go to `http://localhost:4000`

### Exploring the minimesos files

```
$ cat minimesosFile
$ cat es.json
$ cd .minimesos
```

### Destroying the cluster

```
$ minimesos destroy
```

* Show that everything is cleaned up

```
$ docker ps
```
