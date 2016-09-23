#The mess


<pre>
    <code data-trim data-noescape>
docker run -p 25:25 -p 127.0.0.1:2222:22 -d -name postfix linux/postfix:production /usr/bin/supervisord --nodaemon

docker run -p 587:587 -p 25:25 -p 127.0.0.1:2222:22 -d -name postfix-prod linux/postfix:productionv3 /usr/bin/supervisord --nodaemon



docker run -p 8080:8080 -d -name jetty jettyAndCargo:latest java -Djetty.home=/opt/jetty -jar /opt/jetty/start.jar
 </code>
</pre>

 * Docker compose to the rescue!!

