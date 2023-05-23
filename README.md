FFmpegVideoComponent for JUCE projects
=========

This project implements an alternative video component for JUCE using FFmpeg for decoding file based video streams. The component is embedded in a simple example program to demonstrate how it could be used. 
I developed this on Mac OS X and Windows. I am sure it is relatively easy to use it on linux machines as well.
Please keep in mind, that I tested this with my h.264 files only. It might work with other codecs, too, but I can’t guarantee it. I might consider to develop support for more codecs in the future.


## Why?

I developed this video component, because the standard video component of JUCE is not capable of playing back video files using h.264 encoding on a vanilla windows (meaning no third party codecs installed). Another issue I had with the standard video component is the fact, that is impossible to draw something over it. Both problems can be tackled using this FFmpegVideoComponent.

This project is heavily based on Daniel Walz’s [filmstro_ffmpeg](https://github.com/filmstro/filmstro_ffmpeg). With his permission I transformed his code into this VideoComponent. 
He also developed a newer and more feature heavy video module using JUCE and FFMpeg: [foleys_video_engine](https://github.com/ffAudio/foleys_video_engine) 
Check out his projects here: [foleysfinest](https://forum.foleysfinest.com/)


## Installation

1. Use git clone to get a copy of the repository

2. Compile FFmpeg for your machine

This is important! Read „Compiling FFmpeg - OSX.txt“ or „Compiling FFmpeg - Windows.txt“ for more information. A precompiled version of FFmpeg will most likely not work, neither on windows nor mac.

I saved FFmpeg's source code at "PROJECT/ffmpeg/src". I keep the compiled ffmpeg data at "PROJECT/ffmpeg/osx_arm" or "PROJECT/ffmpeg/osx_win". If you choose to save your FFmpeg version elsewhere, make sure to change the post build scripts at "PROJECT/Scripts", so FFmpeg can ne found when for linking. 

3. Use Projucer to create projects for Xcode or Visual Studio. 


## Background




# License
The MIT License (MIT)

Copyright (c) 2022-2023, Clemens Bergthaller

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
