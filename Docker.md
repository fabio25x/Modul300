---


---

<h1 id="markdown-fabio-perrone">Markdown Fabio Perrone</h1>
<p>In diesem File finden Sie die Dokumentation vom Modul 300.</p>
<h2 id="ausgangslage">Ausgangslage</h2>
<p>Ich habe als Ausgangslage eine Ubuntu VM genommen. Auf dieser habe ich Docker installiert.</p>
<h2 id="docker">Docker</h2>
<h3 id="installation">Installation</h3>
<p>Für die Installation habe ich die Anleitung von diesem Link durchgearbeitet:<br>
<a href="https://docs.docker.com/install/linux/docker-ee/ubuntu/">https://docs.docker.com/install/linux/docker-ee/ubuntu/</a></p>
<h3 id="container-erstellen">Container erstellen</h3>
<p>Damit man ein Container erstellen kann, braucht man ein dockerfile</p>
<p>Um ein Webserver zu installieren habe ich dieses dockerfile verwendet:</p>
<pre><code>FROM ubuntu

RUN apt-get update
RUN apt-get install -y apache2 &amp;&amp; apt-get autoremove

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80

CMD ["/usr/sbin/apache2", "-D", "FOREGROUND"]
</code></pre>
<pre><code>docker build -t apache2 .
</code></pre>
<pre><code>docker run -ti apache2 /bin/bash
</code></pre>
<p>Mit exit kann man dann die Verbindung abbrechen.</p>
<h2 id="sicherheit">Sicherheit</h2>
<p>Firewall</p>
<pre><code>root@f45cc37f9f6a:/# ufw status
Status: inactive
root@f45cc37f9f6a:/# ufw enable
Firewall is active and enabled on system startup
root@f45cc37f9f6a:/#
</code></pre>
<p>Memory</p>
<pre><code>docker run -m 2096m --memory-swap 2096m
</code></pre>
<p>Max Anzahl Megabite die einem Container zur verfügung stehen.</p>
<h2 id="testing">Testing</h2>
<p>Container<br>
<img src="https://perrone.myqnapcloud.com:450/share.cgi/Bildschirmfoto%202018-04-17%20um%2014.15.59.png?ssid=02YbC2K&amp;fid=02YbC2K&amp;path=%2F&amp;filename=Bildschirmfoto%202018-04-17%20um%2014.15.59.png&amp;openfolder=normal&amp;ep=" alt="alt-text"></p>
<h2 id="hilfreiche-commands">Hilfreiche Commands</h2>

<table>
<thead>
<tr>
<th>Beschreibung</th>
<th align="center">Command</th>
</tr>
</thead>
<tbody>
<tr>
<td>Alle Docker Stoppen</td>
<td align="center"><code>docker stop $(docker ps -a -q)</code></td>
</tr>
<tr>
<td>Alle Docker Löschen</td>
<td align="center"><code>docker rm $(docker ps -a -q)</code></td>
</tr>
<tr>
<td>Docker erstellen</td>
<td align="center"><code>docker build -t Docker_NAME:Version .</code></td>
</tr>
<tr>
<td>Docker starten</td>
<td align="center"><code>docker run Docker_NAME:Version</code></td>
</tr>
</tbody>
</table>
