# Wurst Noise Library (Circle CI Test)

[![CircleCI](https://circleci.com/gh/eGlint/wurstNoiselib.svg?style=svg)](https://circleci.com/gh/eGlint/wurstNoiselib)

[Version 1.2.0](CHANGELOG.md) 

This repository contains [Kenneth Perlin's Improved Noise](https://mrl.nyu.edu/~perlin/noise/), [Kurt Spencer's Open Simplex](https://gist.github.com/KdotJPG/b1270127455a94ac5d19), and implemented it to Wurst.

Visit [this repository](https://github.com/eGlint/Warcraft-III-Perlin-Noise) for JASS, vJASS, and Lua versions of the Noise library.

If you are not familiar with adding octaves to Perlin Noise, [Flafla2's Octave Perlin](https://flafla2.github.io/2014/08/09/perlinnoise.html), is an optional package that can help you.

## Setup

Before using the noise functions, you need to know the values in the permutation table are now randomly generated (uses Warcraft III's GetRandomInt) during initialization by [default](wurst/Noise.wurst#L234).

If you are having any issues with your noise functions during initialization, your permutation table is possibly uninitialized. 

In case your library that uses the noise functions initializes ahead of the Noise library's initialization, call `Noise.initialize()` in your initializer.
