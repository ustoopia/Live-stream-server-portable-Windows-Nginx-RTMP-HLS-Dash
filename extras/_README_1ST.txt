These little extra's are included because they can help us setup a running
version of Nginx and expand it with some features that might be of interest
to you. Here's what they all do individually:

"ffmpeg" we can use to transcode the live-stream for adaptive bitrate live-
streaming. Important to add the location to your Windows path. See video.

"RunHiddenConsole.exe" is used to start an instance of php-chi.exe on port 9000.
It's on that some port that Nginx can call on it to have it process php files.
Using RunHiddenConsole allows a command to be used just as on the command prompt
but it will not leave you with a dos prompt window that is running something
and should be left alone. This app hides is from view so no accidental 
interaction is performed on this window. It makes no sense to leave it open.

"htpasswd.exe" was built to copy the behaviour of the well-know apache command 
on a linux machine. It's a command prompt app that helps you to protect web-
folders by creating a username & password and the appropriate .htaccess files.
To get help on using this command just try it, since it will tell you what to do.

ramdisk_setup v4.0.2.exe is very, very optional. This app creates a ramdisk 
on your Windows machine that you can have Nginx make use of. And it can do
so perfectly because Nginx loves ramdrives to store it's caching files on.

VC_redist.x64-2019.exe is MS Visual Studio Redistributeable 2015-2019 (x64)
VC_redist.x86-2019.exe is MS Visual Studio Redistributeable 2015-2019 (x86)

These two are required to have installed if you want PHP to work properly.
