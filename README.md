# Live-stream-server-portable-Windows-Nginx-RTMP-HLS-Dash
This zip file will allow you to start live-streaming in a matter of minutes! Unzip it to any location, preferably a USB drive

This package was forked from SwampApe/nginx-rtmp-1.17.10-windows.

What is this? It's my attempt to make it as easy as possible to set up a live-stream 
server on MS Windows.

First we need to make sure that all the files are unblocked by Windows so we can run them.
You can accomplish this by right-clicking the executable files and choose properties, and
then choose unblock. But there is a faster, easy way to unblock all the files in a certain
folder. Click start, start typing: "Windows Powershell" and if it appears, right click on
it and choose: "Run as administrator". Enter something like the following in the window.
(In this example I placed the contents of the zip file in C:\livestream.

dir C:\livestream -Recurse | Unblock-File

dir C:\livestream\extras -Recurse | Unblock-File

Please use your brain here, and do this for the locations where you unzipped the file.

Before you run nginx.exe make sure that you have had a look at the conf/nginx.conf file. It 
might be required to edit some things in there according to you needs or wishes.

Every time you make a change in the configuration, you should use the test-config.bat file
to see if nginx finds any errors in your config. If it finds no errors, you can safely
(re)start Nginx. If it does find an error, it will show you what it is so you can easy
change that option and then try test-config.bat again. 

You need to restart nginx.exe every single time you made changes to the config file. The
config file gets loaded during startup of Nginx so it makes sense that you must restart 
it if you want it to pick up your edited changes. First use the stop-nginx.bat file and 
check if it kills all the nginx processes by looking at your task manager (ctrl+alt+del).
If it doesn't kill all nginx processes you must kill them manually by right-clicking them
and choose "end process". Now you can start nginx.exe again and your changes will be active.

When you want to test the setup, please make sure you set your OBS or any other live-stream
application correctly. The stream URL should be: "rtmp://localhost/live" and the live-
stream key should be: "stream"

If you have any questions, please feel free to NOT bother me about it. Just use google like 
any other well respected geek.

Good luck with it and have fun live-streaming!


# nginx-rtmp-1.17.10-windows

    Nginx: 1.17.10
    RTMP Module: 1.2.1

Used autoconf settings:

auto/configure \
    --with-cc=cl \
    --with-debug \
    --prefix= \
    --conf-path=conf/nginx.conf \
    --pid-path=logs/nginx.pid \
    --http-log-path=logs/access.log \
    --error-log-path=logs/error.log \
    --sbin-path=nginx.exe \
    --http-client-body-temp-path=temp/client_body_temp \
    --http-proxy-temp-path=temp/proxy_temp \
    --http-fastcgi-temp-path=temp/fastcgi_temp \
    --http-scgi-temp-path=temp/scgi_temp \
    --http-uwsgi-temp-path=temp/uwsgi_temp \
    --with-cc-opt=-DFD_SETSIZE=1024 \
    --with-pcre=objs/lib/pcre-8.44 \
    --with-zlib=objs/lib/zlib-1.2.11 \
    --with-openssl=objs/lib/openssl-1.1.1d \
    --with-openssl-opt=no-asm \
    --with-http_ssl_module \
    --with-http_flv_module \
    --with-http_geoip_module \
    --with-http_gzip_static_module \
    --with-http_mp4_module \
    --with-http_secure_link_module \
    --with-http_slice_module \
    --with-http_v2_module \
    --with-mail \
    --with-mail_ssl_module \
    --with-stream \
    --with-stream_ssl_module \
    --add-module=nginx-rtmp-module \
    
