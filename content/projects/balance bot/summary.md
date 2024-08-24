---
title: "FPGAsteroids"
description: "FPGAsteroids"
link: https://github.com/qduff/infoproc-coursework
screenshot: dera.png
date: '2024-03-19'
layout: 'portfolio'
draft: false
---

I worked in a team of 5 to develop a cloud hosted, multiplayer Asteroids game, using an FPGA dev-kit as a controller. The system utilizes a diverse tech stack. A system-verilog implemented and matlab tuned Kalman filter to provide a smooth input to the client over uart. The client is a multithreaded python project comprised of a graphical interface based on the OpenGL wrapper RayLib, a text based interface for the lobby system, an interfave with the FPGA controller, and of course interfacing with the server. The server ran on multithreaded rust, capable of hosting several games simultaneously whilst providing an SQLite poowered lobby system, allowing players to easilly co-ordinate matches and track their performance.

The system is verry performant, with raylib's effiient rendering generating 3700 fps on a desktop with a midrange gpu, tickrate and netcode creating an unnoticable 55ms delay, and the rust server being able to handle 2000+ lobbies at 25% cpu usage, limited by linux kernal restrictions.
