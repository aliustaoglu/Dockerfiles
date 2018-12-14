My GUI apps for Docker that runs in Windows/macOS host

Need to install VcXsrv Windows X Server for Windows or xQuartz for MacOS.

Set your IP

IP=$(ifconfig en0 | grep 'inet ' | awk '{print $2}')
  or manually
IP=192.168.1.37

For macOS you also need to execute below:

`xhost + $IP`

Then for Windows run:

`docker run --rm -it -e DISPLAY=192.168.1.68:0.0 aliustaoglu/scite`

For macOS:

`docker run --rm -e DISPLAY=$IP:0 -v /tmp/.X11-unix:/tmp/.X11-unix aliustaoglu/scite`


To build:
`docker build -t aliustaoglu/scite . `

http://www.linuxandubuntu.com/home/50-essential-linux-applications