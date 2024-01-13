# kazei.dev

## About

My portfolio site. Work in progress. 

Computers are thought of as a tool, or an appliance, but each medium is the content for the next medium to come. Will computers be content? Or will they be interfaces to content?

Originaly written on January 9th, 2024 in a couple hours as a challenge. The idea is to combine my love for Linux/Unix with my recent spat of 3d web development. To save time I glued JSLinux to Aframe with the dom-to-image library. The result is a 3d terminal that can functionally run Linux in a game-engine-like experience. 

Tech being used:

- [**Three.js**](https://threejs.org/)
    - wrapper for WebGL
- [**Aframe**](https://aframe.io/)
    - wrapper for Three.js with some WebAR/WebVR features
- [**JSLinux**](https://bellard.org/jslinux/)
    - a javascript x86/RISCV emulator

## TODO

- [ ] Remove flickering from texture swapping incorrectly.
    - [github discussion with good advice on this very issue](https://github.com/mrdoob/three.js/issues/9337)
- [ ] Find a way to mount the filesystem and upload more files and programs.
- [ ] Add an apartment environment to the scene.
- [ ] Keyboard for mobile.
- [ ] Get the JSLinux websocket networking working so we can use lynx.


## JSLinux README

You must copy all the files to a directory on a web server in order to
run the demo (it is needed so that the XML HTTP Requests work
correctly). Assuming it is installed in http://localhost/jslinux,
explore in a browser:

http://localhost/jslinux

A minimal busybox distribution for RISCV-64 and x86 is provided. The
RISCV-64 version is executed by default. To run the x86 version,
explore:

http://localhost/jslinux?cpu=x86

The source jslinux.js can be modified to change the default
configuration.

More complete Linux distributions (such as buildroot) can be used
provided you keep using the same precompiled Linux kernels. The
TinyEMU 'splitimg' tool must be used to convert a diskimage to a list
of files. For example:

splitimg root-riscv64.bin root-riscv64 256

The demo VM configurations are in root-riscv64.cfg and root-x86.cfg.
