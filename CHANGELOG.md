# Changelogs for Wurst Noise Library

    v1.2.0
        - Added Noise.initialize, and it is called during initialization by default
        - Added NoiseRandom interface
        - Added a new overload for Noise.generateRandomPermutation: Noise.generateRandomPermutation(NoiseRandom)
        - Added Noise.version

    v1.1.0
        - Added the Noise.openSimplex(vec2) function
        - Now supports chillup [#1]
        - Replaced real.lerp() with linear() [#2]
        - Added unit testing [#2]
        - Added documentation [#2]

    v1.0.1
        - Removed lerp() and used the one in the standard library: real.lerp()

    v1.0.0
        - Initial release
