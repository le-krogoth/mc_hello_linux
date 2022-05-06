# mc_hello_linux
Small project to test platformio for Linux x86_64 platform

# Howto
## make sure that Debian loads ./local/bin into the Path from .profile
> mkdir ~/bin

## if not already installed
> sudo apt install python3-pip

## install / update platformio to latest
> pip install -U platformio

## go to your dev folder
> cd ~/my-dev-folder

## make new and enter dev directory
> mkdir mc_hello_linux 
> cd mc_hello_linux/

## Initialise platformio


## Change config accordingly

> nano platformio.ini

`
; PlatformIO Project Configuration File
;
;   Build options: build flags, source filter, extra scripting
;   Upload options: custom port, speed and extra flags
;   Library options: dependencies, extra library storages
;
; Please visit documentation for the other options and examples
; http://docs.platformio.org/page/projectconf.html

[env:linux_x86_64]
platform = linux_x86_64
`

## Write the hello world source file

> nano src/main.c

`
#include <stdio.h>

int main()
{
    printf("Hello World!\n");
    return 0;
}
`

# Compile / Build project
> pio run

# Run program
> .pioenvs/native/program

# Clean build files
> pio run --target clean




# Short route for cheaters
# Get this project
> git clone https://github.com/le-krogoth/mc_hello_linux.git

## Enter directory
> cd mc_hello_linux/

# Compile / Build project
> pio run

# Run program
> .pioenvs/native/program

# Clean build files
> pio run --target clean
