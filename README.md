# Nodejs app to change background in ICEWM
<hr/>
<h3>A Nodejs application to change background image in ICE window manager</h3>
<p>ICEWM, ICE window manager is a useful way to reduce memory use in linux 
distributions.  However, ICE comes with little to no simple methods for doing many desktop tasks.</p>
<p>I recently changed my Fedora laptop to ICEWM. Though I knew the manager from running AntiX in the past, I realized AntiX had more desktop tasks set up than plain ICEWM.  One can change the background image in a configuration file ($HOME/.icwem/menu) or with the icewembg command. I prefer something simpler than a long complicated command.</p>
<p>So, needing some Nodejs practice and a better mousetrap, I wrote icechngbg.  It's pretty simple and can be moved into /bin as it is set up to be an independent executable.</p>
<p>The app is not a permanent setting and will be erased any time a new session of ICEWM is started.  For a permanent setting, place your choice in the "menu" config file.</p>
<p>If you just want the executable script, it is the one without an ending.</p>
<p>As always, use at your own risk.</p>