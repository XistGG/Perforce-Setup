# Perforce Setup

This repository contains sample files to help you set up your own P4 server.

`typemap.txt` should be used like `cat typemap.txt | p4 typemap -i`
**before** you try to add any files to P4.

`.p4ignore` must be the very first thing you commit to your P4 depot,
to ensure that all files you add thereafter are files you actually want
to keep in P4.

# See also

[https://x157.github.io/Perforce/](https://x157.github.io/Perforce/)
