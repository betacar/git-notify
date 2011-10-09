git-notify
========

Originally forked from [jakeonrails / git-notify](https://github.com/jakeonrails/git-notify).

This little bash script will watch your origin/master for updates every 60 seconds and uses notify-send to alert you of new commits.

Usage:
----------

Save it under the following directory to use it as a command: 
    /usr/local/bin

then,

    $ git-notify ~/code/some-git-repository origin/master &

or a is the same,
    $ git-notify [project_folder_path] [branch_to_monitor] &

The ampersand (&) at the end tells your terminal to launch it in the background. If you want to kill it later, you can do:

    ps aux | grep git-notify

Which will output something like:

    jake      9541  0.0  0.0  12012  1392 pts/3    S    12:54   0:00 /bin/bash ./git-notify
    jake      9558  0.0  0.0   8952   876 pts/3    S+   12:55   0:00 grep --color=auto git-notify

Note the first number in the list, 9541, that is the PID of the script. You can now terminate it like so:

    kill 9541

Installation:
------------
Just download git-notify and put it somewhere in your path.

Jake Moffatt, jakeonrails@gmail.com
Carlos Betancourt, carbetacar@gmail.com
