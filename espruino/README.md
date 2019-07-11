Use this Docker image to flash Espruino firmware and upload program to ESP8266 or ESP32.

It uses `espruino-create-project` to create boilerplates.

https://www.npmjs.com/package/espruino-create-project

If you're using macOS, you'll need to be able to access the USB port that your ESP chip connected to. Since Docker now uses native drivers (not Virtual Machine) we need to tell Docker to switch to Virtual Machine. We can later on switch using native drivers.

Install docker-machine if you don't have

https://docs.docker.com/machine/install-machine/

Create 

```bash
docker-machine create --driver virtualbox default
```

Now we need to add the USB device to the Virtual Machine.

First stop docker machine

```bash
docker-machine stop
```

And open VirtualBox and find your image (named default)

![VirtualBox](https://raw.githubusercontent.com/aliustaoglu/Dockerfiles/master/espruino/pics/virtualbox.png)

And make USB device available from the virtual machine

![VirtualBox](https://raw.githubusercontent.com/aliustaoglu/Dockerfiles/master/espruino/pics/usbdevice.png)

Inside the image it will be something like this. And this name is important.

```
/dev/ttyUSB0
```

Now set the environment to be the one we've created above

```bash
eval "$(docker-machine env default)"
```

Then follow steps below on how to create boilerplate and use the port you've created above.

https://www.npmjs.com/package/espruino-create-project


When you finish and want to switch back to native drivers run below:

```bash
eval $(docker-machine env -u)
```