Another Virtualization technology??

## Hipster fad?? {% fragment %}
  <img class="plain" src="resources/images/hipsterBeard.jpg" style="width: 25%"></img> {% fragment %}

** Nope {% fragment %} **


Note:

So you know, a lot has been said about docker

but why the hell are they reinventing the wheel with another virtualization

Is docker simply a product of bored techies that are reinventing the wheel?? {% fragment %}

do we need another one of these?


--

## No overhead

<img class="plain" src="resources/images/contvsvm.png" style="width: 100%"></img>

<footer style="text-align: left;"><small><small><a href="https://twitter.com/jonasrosland" target="_blank">©jonasrosland</a></small></small></footer>


Note:

How many of you have worked with Vagrant and other virtualization tools for deployment?

The overhead of the harddrive and the CPU/etc overhead

You might be saying, oh great, so we get this new whole set of tools just to shave off some CPU cycles and eventually some bytes?

Not quite

Less isolation

--

## Container - the analogy
<img class="plain" src="resources/images/containerAnalogy.png" style="width: 100%"></img>
<footer style="text-align: left;"><small><small><a href="https://twitter.com/jonasrosland" target="_blank">©jonasrosland</a></small></small></footer>


--

## Container - the analogy
<img class="plain" src="resources/images/techAnalogy.png" style="width: 100%"></img>
<footer style="text-align: left;"><small><small><a href="https://twitter.com/jonasrosland" target="_blank">©jonasrosland</a></small></small></footer>


--

# Solution
<img class="plain" src="resources/images/container.png" ></img>

#### The real MV..Concept 

--

Don't have to deal with:
 * Configuring the development environment in the workstation {% fragment %}
 * Configuring the production environment in the server {% fragment %}
 * Configuring the continuous integration environment in the server {% fragment %}
 
 
## One Container to rule them all {% fragment %}
## How ?? {% fragment %}


Note:

The idea is that you don't have to configure your development environment, you don't configure

