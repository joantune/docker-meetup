## Container solution

**cgroups** (abbreviated from control groups) is a Linux kernel feature that limits, accounts for, and isolates the resource usage (CPU, memory, disk I/O, network, etc.) of a collection of processes.

 * Engineers at Google (primarily Paul Menage and Rohit Seth) in 2006 {% fragment %}
 * Docker is built on top of that, but it provides much more {% fragment %}
 

--

## Container solution


### Local filesystem changes

# 🤔 {% fragment %}

--

## Container Solution
<img class="plain" src="resources/images/pushAndPullTransparent.png" ></img>
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

## Container Solution - Dockerfile

### Volumes - mounting local directories