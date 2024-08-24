---
title: "FPGAsteroids"
description: "FPGAsteroids"
link: https://github.com/qduff/infoproc-coursework
screenshot: dera.png
date: '2024-03-19'
layout: 'portfolio'
draft: false
---

I worked in a team of 5 to develop a cloud hosted, multiplayer Asteroids game, using an FPGA dev-kit as a controller. The system utilizes a diverse tech stack. A system-verilog implemented and Matlab tuned Kalman filter to provide a smooth input to the client over UART. The client is a multithreaded python project comprised of a graphical interface based on the OpenGL wrapper RayLib, a text based interface for the lobby system, an interface with the FPGA controller, and of course interfacing with the server. The server ran on multithreaded rust, capable of hosting several games simultaneously whilst providing an SQLite powered lobby system, allowing players to easily co-ordinate matches and track their performance.

The system is very performant, with RayLib's efficient rendering generating 3700 fps on a desktop with a midrange GPU, tick-rate and net-code creating an unnoticeable 55ms delay, and the rust server being able to handle 2000+ lobbies at 25% CPU usage, limited by Linux kernel restrictions.
