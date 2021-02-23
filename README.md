# OctoPrint-Gpioshutdown

GPIO Shutdown is a simple plugin that can shutdown the Raspberry Pi if a switch connected to ground and one of the GPIO pins pressed. This plugin also turns On a led when Octoprint server is up and running. Connect a led to one of the GPIO pins and other end to ground, then set the pin number (BCM Mode) in plugin settings in web interface.

<img src="https://github.com/fmalekpour/OctoPrint-Gpioshutdown/blob/master/screenshots/gpio-shutdown_bb.jpg?raw=true" width="500px">

## Updates over original

Added the option to use GPIO 3 as a shutdown pin as many users use this pin to turn on their pi, it makes sense to have one button for on/off
Also added the option to use GPIO 3 as an LED pin because why not

## Setup
In plugin manager from URL:
    ```https://github.com/GoldenGorilla123/OctoPrint-Gpioshutdown-Inclding-GPIO3/archive/master.zip```

Via command line:
    ```pip install "https://github.com/GoldenGorilla123/OctoPrint-Gpioshutdown-Inclding-GPIO3/archive/master.zip"```


## Configuration

In web interface, install the plugin and reload if necessary, then click on GPIO Shutdown, you will have:

- Pin Shutdown: Raspberry Pi GPIO pin (BCM Mode) your shutdown switch is attached to.
- Pin Led: Raspberry Pi GPIO pin your ready-to-run led attached to. This led will turn On when OctoPrint is up and ready to run/connect.
- Debounce Time: When press the shutdown switch, wait for this amount of time to wait for the signal to stabilize.

<img src="https://github.com/fmalekpour/OctoPrint-Gpioshutdown/blob/master/screenshots/screen01.jpg?raw=true" width="500px">

You can find the GPIO pin number assignments at [Raspberry Pi GPIO Pinout](https://www.raspberrypi.org/documentation/usage/gpio/).

