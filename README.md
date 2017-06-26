# XM
XM is a Linux Script for downloading flash based videos and turning them into mp3 from flash video hosts, it was created for understanding of how linux works, and bash itself. i created it, to streamline the process of utilizing applications in a certain method.

included with the script is three files.

xm-start -yt link   |  get the video, makes the mp3.

xm-clean            |  clean the libary and delete all content.

xm-set              |  set the audio libary location and metafile data.

What does this script do?

It downloads a flash video in MP4 format, Stores it, renames it, converts it to mp3 and then deletes its MP4 source video instantly.

It stores a single audio track in a nested folder called Youtube if you select the -yt option, you need to create this folder in your $USER directory. The script now does this for you autmatically. 

you can use the script ./xm-set to set first time setup. this creates the folder in your user directory.

you can use the script ./xm-clean to clean the libary and reset the metafile

you can use the script ./xm-start -yt and the link

Hope you like it.
Hope it helps you.
Hope you add too it.

# How to use the script?
run ./xm-start -yt https://www.youtube.com/watch?v=-hJf4ZffkoI 
it will get the video. 
download it. 
convert it. 
delete the video. 
and add the mp3 to its own metadata libary.

so simple. its intellectually wonderful. but the speed of the task depends on the size of the video source.

# Metadata file
there is a metadata file ( xmusic.meta ) created to handle the metainfo of the video.
it gets the name from you, the url for the track, gives it a unique identifier, 
sets it up so the metadata can easily be ported to a frontend gui, 
which is the final goal of this project, also, with ability 
to have custom front end for both Xubuntu 16.04 and Jessie 8

# FFMPEG in Jessie 8
this script needs a backport of FFMPEG in order to work, so 
add the backport url needed for your os.
e.g. sudo nano /etc/apt/sources.list/
and add this line.
# backports
deb http://ftp.uk.debian.org/debian jessie-backports main contrib non-free
sudo apt-get update
sudo apt-get install ffmpeg

and if your video is small in size, watch how fast it runs. 
even on an old machine like the one the script has been made on.

# Signiture Error in the APT/APTITUDE package.
Resolved by installing the PIP Package, 
Make sure to remove with APT the older package of youtube-dl

First Install PIP | (sudo apt-get install pip)
Second Install | (sudo pip install youtube-dl)
