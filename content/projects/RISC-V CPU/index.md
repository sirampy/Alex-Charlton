---
title: "RISC-V CPU"
description: "A RISC-V CPU implemented in sysem verilog"
link: https://github.com/sirampy/Team22
date: '2024-03-19'
layout: 'portfolio'
draft: false
weight: 70
---
I worked in a team of 6 to develop a RISC-V CPU inverilog from scratch. The processor succesfully implemented the entire RISC-V base instruction set, verified agains a set of test programs. Different iterations of the CPU were also developed, including a version with a Two-Way Set-Associative cache controller, and a pipelined version with an advanced hazard detection unit. I worked mostly on the core processor, figuring out the optimal way to decode an excecute the instructions. I also automated the build and test system using make and python to compile the RTL (using verilator), compile the assembly files and set the correct data memory hex files to be used by verilator. This ended up being the core framework that all team members used to run their tests, saving a lot of time.

## How I optimized the microarchitecture

I wanteed to re-use as manny hardware components as possible within each pip
