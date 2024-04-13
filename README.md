# Gazebo (Non-Classic)

This repository keeps notes on the common issues with Gazebo (non-classic). Brace yourself!

## Installation

Ubuntu 22.04
```bash
ansible-pull -U https://github.com/brucechanjianle/ansible-gazebo -K -C harmonic
```

## Usage

Start example world that has a little tugbot.
```bash
gz sim "https://fuel.gazebosim.org/1.0/openrobotics/worlds/tugbot in warehouse"
```

Surely, you will face with lots of error! And it will not LOAD :(
But not to worry, below are the fixes :D
```bash
# Errors
# libcurl: (6) Could not resolve host: fuel.ignitionrobotics.org
# [Err] [FuelClient.cc:695] Failed to download model.
#   Server: https://fuel.ignitionrobotics.org
#   Route: movai/models/shelf/tip/shelf.zip
#   REST response code: 0
# [Err] [RestClient.cc:336] Error in REST request

cd ~/.gz/fuel
fgrep -r "ignitionrobotics" in the url to "gazebosim"
# Refer: https://github.com/gazebosim/gz-sim/issues/2281
```
