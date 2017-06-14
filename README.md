# Dashing
A [Docker](http://docker.io/) Container for [Dashing] (http://dashing.io/)



Link: [musanmaz/docker-dashing](https://registry.hub.docker.com/u/musanmaz/docker-dashing)


## Run
```docker run -d -p 3030:3030 musanmaz/docker-dashing```

And point your browser to [http://localhost:3030/](http://localhost:3030/).


## Configuration

### Dashboards
To provide a custom dashboard, use container volume **/dashboards**:

```docker run -v=/my/custom/dashboards:/dashboards -d -p 3030:3030 musanmaz/docker-dashing```

(*Don't forget to also provide the layout.erb*)

### Jobs
To provide custom jobs, use container volume **/jobs**:

```docker run -v=/my/cool/job:/jobs -d -p 3030:3030 musanmaz/docker-dashing```

### Widgets
To install custom widgets supply the gist IDs of the widgets as an environment variable:

```docker run -d -e WIDGETS=5641535 -p 3030:3030 musanmaz/docker-dashing```

### Public (favicon, 404)
To provide custom 404 and favicon, use container volume **/public**.

### Configuration File
The configuration file ```config.ru``` is available on volume */config*.

Edit this file to change your API key, to add authentication and more.

### lib volume
The dashing lib dir is available on volume */lib-dashing*.
