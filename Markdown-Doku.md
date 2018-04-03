---


---

<h1 id="markdown-fabio-perrone">Markdown Fabio Perrone</h1>
<p>In diesem File finden Sie die Dokumentation vom Modul 300.</p>
<h2 id="ausgangslage">Ausgangslage</h2>
<p>Ich habe als Ausgangslage eine Ubuntu VM genommen. Auf dieser habe ich Virtualbox installiert.</p>
<h2 id="github">GitHub</h2>
<p>Git installation<br>
<code>sudo apt-get install git</code></p>
<p>Um verschiedene Beispiele auf der VM zu haben, habe ich die devops Repository auf meiner VM geclont.</p>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> config --global user.name<span class="token string">"fabio25x"</span>
<span class="token function">git</span> config --global user.email <span class="token string">"fabio.perrone@edu.tbz.ch"</span>
<span class="token function">git</span> clone https://github.com/mc-b/devops
</code></pre>
<p>Um immer die Dateien auf dem aktuellsten Stand zu haben, hat Julian ein Skript geschrieben.</p>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> status
<span class="token function">git</span> add Dokus/
<span class="token function">git</span> push
<span class="token function">git</span> commit -m <span class="token string">"Dokus"</span>
<span class="token function">git</span> push -u origin master
</code></pre>
<h2 id="vagrant">Vagrant</h2>
<h3 id="installation">Installation</h3>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">apt-get</span> <span class="token function">install</span> vagrant
</code></pre>
<h3 id="vm-erstellen-und-benutzen">VM erstellen und benutzen</h3>
<p>Ein neues Vagrantfile erstellt man mit diesem Befehl:</p>
<pre class=" language-bash"><code class="prism  language-bash">vagrant init ubuntu/xenial64 
</code></pre>
<p>Im Verzeichnis welches das Vagrantfile liegt kann man dann</p>
<pre class=" language-bash"><code class="prism  language-bash">vagrant up
</code></pre>
<p>die Virtuelle Maschine starten.</p>
<p>Zum sich auf die VM zu verbinden kann man diesen Befehl verwenden:</p>
<pre class=" language-bash"><code class="prism  language-bash">vagrant <span class="token function">ssh</span>
</code></pre>
<p>Das Vagrantfile welches ich erstellt habe ist im GitHub zu finden.</p>
<h2 id="testing">Testing</h2>
<p>Nachdem ich die VM mit Vagrant gestartet habe, meldete ich mich mit vagrant ssh auf die VM ein und überprüfte ob die gewünschten Prozesse laufen.</p>
<p>Apache:<br>
<img src="https://perrone.myqnapcloud.com:450/share.cgi/Prozesse%20Apache.png?ssid=02YbC2K&amp;fid=02YbC2K&amp;path=%2F&amp;filename=Prozesse%20Apache.png&amp;openfolder=normal&amp;ep=" alt="alt-text"></p>
<p>Website:<br>
<img src="https://perrone.myqnapcloud.com:450/share.cgi/Bildschirmfoto%202018-03-27%20um%2014.31.15.png?ssid=02YbC2K&amp;fid=02YbC2K&amp;path=%2F&amp;filename=Bildschirmfoto%202018-03-27%20um%2014.31.15.png&amp;openfolder=normal&amp;ep=" alt="alt-text"></p>
<p>Firewall:<br>
<img src="https://perrone.myqnapcloud.com:450/share.cgi/Firewall.png?ssid=02YbC2K&amp;fid=02YbC2K&amp;path=%2F&amp;filename=Firewall.png&amp;openfolder=normal&amp;ep=" alt="alt-text"></p>

