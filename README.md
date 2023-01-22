# Perforce Setup

This repository contains sample files to help you set up your own P4 server
for an Unreal Engine project.

[`typemap.txt`](https://github.com/XistGG/Perforce-Setup/blob/main/typemap.txt)
should be used like `cat typemap.txt | p4 typemap -i`
**before** you try to add any files to P4.

The `.p4ignore`
should be the first thing you commit to your P4 depot,
to ensure that you do not add unwanted files to P4.

For a project-only depot, use
[`.p4ignore`](https://github.com/XistGG/Perforce-Setup/blob/main/.p4ignore),
for a custom engine root depot, copy
[`engine-root.p4ignore`](https://github.com/XistGG/Perforce-Setup/blob/main/engine-root.p4ignore)
as `.p4ignore`.


# See also

[https://x157.github.io/Perforce/](https://x157.github.io/Perforce/)

[https://x157.github.io/Perforce/p4ignore](https://x157.github.io/Perforce/p4ignore)

[https://x157.github.io/Perforce/Typemap](https://x157.github.io/Perforce/Typemap)
