# systemd service using fluent-bit

This Makefile recipe is for temperature monitoring
using the fluent-bit collecter as a systemd service
on Linux.

Tested on Ubuntu 18.04 and Raspberry Pi.

## Configuration

- NAME service name
  default: `temper-python`
- PREFIX prefix for temper-python and fluent-bit installation
  default: `/usr/local`

## Install

- `sudo make install`

## Start/stop service

- `sudo make start`
- `sudo make stop`

## Service status

- `make status`
- `make logs`

