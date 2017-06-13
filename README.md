# CasparPlayoutServer

This is an CasparCG Playout controller build in PHP. 


## CLI files

There are several PHP files that should be run from the command line. Those are found in the cli_server folder.

worker.php should be run indefintly, it reads playlist files and connect to caspar to do the actualy playout
create_playlist.php should be run every x minutes to update the file read by worker.php 

The reason why we create the playlist file every x minutes is for perfomance reason, the worker should be ploughing through 1000 playlist items to find what it must do, there should be only the next few things it has to do. 
