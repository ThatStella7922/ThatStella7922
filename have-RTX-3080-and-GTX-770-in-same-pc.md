## How I made my GTX 770 work in my PC along my RTX 3080 to provide macOS compatibility

## Introduction
Back on February 4th, I upgraded my PC with a Strix RTX 3080 OC which replaced my previous Vega 56. As you can imagine, this brought about a whole slew of compatibility problems for macOS. The biggest and most devastating one was that the RTX 3080 is not supported in any way in any version of macOS. This means no Web Drivers on High Sierra either. One workaround I used for a while was using macOS with a single monitor in VESA compatibility mode with 1080p resolution thanks to the UEFI GOP, but this was far from ideal. VESA compatibility mode means that there is no acceleration and the CPU must handle rendering tasks. Aside from this making the entire OS feel *extremely* sluggish, it also means that I can't use any macOS apps that use Metal. I had to find another, better solution.

As I use macOS quite a bit on my PC, I wanted to have full resolution and acceleration in macOS
