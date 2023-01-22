# Perforce Setup

This repository contains sample files to help you set up your own P4 server
for an Unreal Engine project.

The `typemap` here will configure the entire server `//...` for the types indicated.
Change that if needed to limit to a specific `//Depot/...`

The `.p4ignore` should be the first thing you submit to P4
to ensure that you do not add unwanted files to the stream.


## Typemap Server Config

[`typemap.txt`](https://github.com/XistGG/Perforce-Setup/blob/main/typemap.txt)
should be used like `cat typemap.txt | p4 typemap -i`
**before** you try to add any files to P4.

Note this configures the entire server `//...` which is fine for a new server.

If you are trying to add this to an existing server, you may wish to modify
the `typemap` to limit its effects to a certain `//Depot/...`
before you `| p4 typemap -i`


## C++ Project Source Depot `.p4ignore`

Source: [`.p4ignore`](https://github.com/XistGG/Perforce-Setup/blob/main/.p4ignore)

This is a `.p4ignore` for a C++ (source-only) Project Source Depot.

This depot is source-only.
Each developer must compile the Project independently
for their own platform.

Building the Project in the `Debug Editor` configuration
will generate all relevant C++ debug symbols, which are
purely-generated massive files IMO not worth keeping in SCM.
These files are vital to aiding in C++ debugging efforts.

For best results, the Engine must also be built in `Debug Editor`,
and/or the debugging symbols must be downloaded via the 
Epic Games Launcher for a packaged Engine build.

## C++ Custom Engine Source Depot `engine.p4ignore`

Source: [`engine.p4ignore`](https://github.com/XistGG/Perforce-Setup/blob/main/engine.p4ignore)

This is a `.p4ignore` for a Custom Engine Source Depot.

This depot is source-only.
Each developer must compile the Engine independently
for their own platform.

Building the Engine in the `Debug Editor` configuration
will generate all relevant C++ debug symbols, which are
purely-generated massive files IMO not worth keeping in SCM.
These files are vital to aiding in C++ debugging efforts.


# See also

[https://x157.github.io/Perforce/](https://x157.github.io/Perforce/)

[https://x157.github.io/Perforce/p4ignore](https://x157.github.io/Perforce/p4ignore)

[https://x157.github.io/Perforce/Typemap](https://x157.github.io/Perforce/Typemap)
