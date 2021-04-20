# balena ROS2 Foxy Base container

[![balena deploy button](https://www.balena.io/deploy.png)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/balena-io-examples/balena-ros2-foxy-base/)

## Special Note:
This GitHub repository is based on the foundational work of Keenan Johnson's repo, located here: https://github.com/keenanjohnson/balena-ros/. Be sure to give Keenan a Star and a Follow!


## About
This repo installs ROS2 into a 64-bit Ubuntu Arm container, ready to be run on a Raspberry Pi 4 or an NVIDIA Jetson Nano running balenaOS.  Other 64-bit Arm platforms might also work, but have not been tested.  The Dockerfile adds the basic requirements, adds the ROS key and APT sources, then installs the ROS binaries.  This repo sets up the ROS2 Foxy "Base" install, which is a minimal, command-line only version.  There is a repo that will be posted soon that is a more thorough version, that installs a Desktop GUI into the container as well... but that makes for a larger container size of course.

## Usage
To get started, you can simply click the "Deploy with balena" button above, or use the traditional workflow and do a `git clone` of this repo, and then a `balena push YourAppNameHere` to deploy the container to your device.  You can read about how to create a balena application, setup your device, and install the balena CLI here:  https://www.balena.io/docs/learn/getting-started/raspberrypi4-64/python/

Once your device is provisioned and online, and the containers have been built and downloaded, you can start using ROS commands.  This repo is a very basic implementation, designed to just give an example of how to get ROS2 installed and running, but there is a small "Talker / Listener" demo that is included.  You can run it by opening up a Terminal session to the `main` container in the balenaCloud dashboard and running `ros2 launch demo_nodes_cpp talker_listener.launch.py`.  Again, this is just a simple publisher and subscriber topic to show that the ROS installation is working.  You'll definitely want to iterate from here, but this container is a great starting point.

![Alt text](/img/screenshot1.png?raw=true)
