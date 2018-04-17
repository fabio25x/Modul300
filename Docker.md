---


---

<h1 id="markdown-fabio-perrone">Markdown Fabio Perrone</h1>
<p>In diesem File finden Sie die Dokumentation vom Modul 300.</p>
<h2 id="ausgangslage">Ausgangslage</h2>
<p>Ich habe als Ausgangslage eine Ubuntu VM genommen. Auf dieser habe ich Docker installiert.</p>
<h2 id="docker">Docker</h2>
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

