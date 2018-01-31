# Termux repository of X/GUI packages
This repository contains various X/GUI packages (such as **dosbox**) that can be used with [Termux](https://github.com/termux/termux-app).

## How to enable this repository
Download and run a [script](https://github.com/xeffyr/termux-x-repository/blob/master/enablerepo.sh) that will automatically add repository to your 'sources.list' file and add public key:
```
wget https://raw.githubusercontent.com/xeffyr/termux-x-repository/master/enablerepo.sh
bash enablerepo.sh
```

## How to run X packages
1. Install package 'termux-desktop' from this repository: `pkg install termux-desktop`.
2. Install VNC viewer. You can use this: https://play.google.com/store/apps/details?id=com.realvnc.viewer.android
3. Create a new session in Termux and type: `startx`. On first launch you will be prompted for setting up a VNC password.
Output of startx should contain something like this 'New ... desktop is localhost:1'. At this point, openbox session will
be launched.
4. Open VNC viewer application and create a new connection to the host 127.0.0.1:5901. Use password entered in step 2 and you will see a desktop.

If you want to launch a X program directly from the Termux, make sure that a variable DISPLAY set to correct display:
```
export DISPLAY=:1
```

## Note
This repository uses Github Pages. Since they are use caching, sometimes when repository is updated you may receive errors like
'Hash Sum mismatch', '404 Not Found', 'Writing more data than expected'. Usually, the problem should gone away in ~10 minutes after
repository was updated.
