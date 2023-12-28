LogView
=======

Small program to view the .klg format.

Requires CMake, Boost, ZLIB and OpenCV.

```sh
cmake -G Ninja -B build
cmake --build build
```

Run like;

```sh
./LogView -l ~/Kinect_Logs/livingRoom2.klg -f -w 640 -h 480
```
