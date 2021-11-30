# Nvidia's HelloAIWorld integration with Isaac

The objective is to adapt the [Nvidia's Hello AI Worl inference tutorial](https://github.com/dusty-nv/jetson-inference) using the Isacc SDK.
The use case is the Object Detection Program.
The extra constrain is to make the Isaac nodes run on a Jetson nano with a Raspberry Pi Camera

## Prerequisites

1. Jetson setup with Jetpack 4.5 (https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit)
2. Setup Isaac Sdk as described (https://docs.nvidia.com/isaac/isaac/doc/setup.html)
    * Deskop installed with Ubuntu 18.04 (In my case, it's a Macbook pro + Parallel Desktop + Ubuntu 18.04 (ubuntu-18.04.6-desktop-amd64.iso))
    * Isaac dependencies installed on Jetson


## Step 1
Setup the project structure under the ./isaac/sdk/apps folder

``` bash
~/isaac/sdk/apps$ git clone https://github.com/z-Index-Otto/Nvidia-HelloAIWorld-Isaac.git
```

> you'll have to adapt the deploy./sh file in order to match to your Jetson's user and IP

As we use a Rapberry Pi camera connected on the Jetson board (CSI), we'll use the `isaac/sdk/apps/samples/argus_camera` as starting point. This sample uses the [isaac.ArgusCsiCamera](https://docs.nvidia.com/isaac/isaac/doc/doc/component_api.html#isaac-arguscsicamera) node type to support CSI camera

## Step 2
Make the [Building Isaac Applications](https://docs.nvidia.com/isaac/isaac/doc/tutorials/building_apps.html) sample working.
Check the (argus_camera/argus_camera.app.json) and the (argus_camera/BUILD) adapted according to our case

