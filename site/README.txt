This is the root web folder. When you open in your browser http://localhost:8050 you will see
a page that is located in this folder. For viewing the HLS livestream open this address:
http://localhost:8050/hls.html and for Dash open http://localhost:8050/dash.html.
Open these files with a text editor to see what they look like so you can use them as an
example on how to integrate the livestreams on your own website.

If you already have your own website setup and want to host it with our running Nginx then
you should place them in this folder. Make sure you have at least one of these index files
included or else your site won't load:

index.htm , index.html , index.php.

Make sure to have a look at the statistics page that can be found when opening /stat

http://localhost:8050/stat

It won't show anything if nobody is live-streaming but once a livestream is incoming
be sure to check it out. Or when you need help in trying to get it all up and running
this can be a great tool to help with this.
