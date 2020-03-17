# mpv-config

This is a collection of [MPV](https://github.com/mpv-player/mpv) configuration files, intended for high quality rendering of traditional live TV and video disc formats. Beyond upscaling, my configuration files include optimizations for resolution, colorspace, dithering, debanding, motion interpolation, and anti-ringing. Additionally, FFMPEG’s bwdif filter for motion adaptive deinterlacing is applied to interlaced video, such as live TV or DVDs.

For now, my mpv.conf is tailored for rendering on Macs (e.g. current iMacs). Because Macs do not support Vulkan and MPV does not support Metal, Mac's deprecated OpenGL subsystem is used. Your performance will vary depending on the Mac that you use. You may need to disable shaders. On Macs, you can download and install them in your ~[user profile]/.config/mpv folder.

If you have a Vulkan-enabled device (e.g. Windows or Linux), you can uncomment the relevant lines to use that graphics subsystem instead of OpenGL. If you are using Windows or have your configuration files in a different location, then you should modify mpv.conf accordingly.

## IINA / libmpv
I like to use the native Mac app [IINA](https://github.com/iina/iina) since it uses libmpv as playback engine. As my mpv.conf uses some specific OSD and OSC settings, IINA will crash on startup. As workaround, I defined an extra folder with a customized mpv.conf for it in ~[user profile]/.config/iina (you have to set the path in IINA advance preferences). Shaders will point to mpv folder. If you want to use this mpv.conf for IINA or any libmpv based player, just disable/remove the lines from mpv.conf
