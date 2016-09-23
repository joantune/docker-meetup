## Container solution

**cgroups** (abbreviated from control groups) is a Linux kernel feature that limits, accounts for, and isolates the resource usage (CPU, memory, disk I/O, network, etc.) of a collection of processes.

 * Engineers at Google (primarily Paul Menage and Rohit Seth) in 2006 {% fragment %}
 * Docker is built on top of that, but it provides much more {% fragment %}
 

--

## Container solution


### Local filesystem changes

# 🤔 {% fragment %}

Note:

-- In docker you have the concept of images and containers, a container is something that is running or that run, and an image is a more persistent thing --


docker ps 
-- to show running containers --

docker ps -a 

-- to show all of the containers, even the ones that are stopped --

-- so, in this example we are running the ubuntu image, which defaults to the latest version, in a new container named testContainer -- 

docker run -t -i --name testContainer ubuntu /bin/bash

Ctrl + p Ctrl + q

docker images

docker commit -m "Initial commit" useless/test


docker diff testContainer 

docker attach testContainer

echo "test" > confFile

<Detach>

docker diff testContainer

docker commit -m "Configured container" useless/test

docker history useless/test


--

## Container Solution
<img class="plain" src="resources/images/pushAndPullTransparent.png" ></img>

<footer style="text-align: left;"><small><small><a href="https://twitter.com/jonasrosland" target="_blank">©jonasrosland</a></small></small></footer>
#### Push and Pull {% fragment %}

--

## Container Solution - Le hub


<a href="https://hub.docker.com/explore/" target="_blank">
	<img class="plain" src="resources/images/leHub.png" style="width: 50%" ></img>
</a>
 * <a href="https://hub.docker.com/_/ruby/" target="_blank">Ruby</a>
 * <a href="https://hub.docker.com/_/redis/" target="_blank">Redis</a>

--

## Container Solution - Dockerfile

<pre>
    <code data-trim data-noescape>
FROM ruby:2.3
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        postgresql-client \
    && rm -rf /var/lib/apt/lists/*
WORKDIR /usr/src/app
COPY Gemfile* ./
RUN bundle install
COPY . .
EXPOSE 3000
CMD ["rails", "server", "-b", "0.0.0.0"]
    </code>
</pre>


--

## Container Solution - Volumes

 * Volumes - mounting local directories
 * Or - data containers, i.e. volumes as containers
 
# 🤔 {% fragment %}
