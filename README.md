Detects whether a camera device is in use by a specified process.

One of the things it can do is turn on a [red light](https://www.blinkstick.com/) when webcam use is detected: 

![light](/docs/light.jpg)

## Configuration

We need to specify the process names we're watching for, the filenames of the webcam devices on our system, and the action we want to take when use is detected.

```yaml
---
# config.yml
#
# List of process name prefixes
process_names:
 - zoom
# List of filenames (partial filenames work as well)
video_files:
 - ["/dev/video", "AppleCamera"]
# Default Action is return value of the program (0=camera is being used)
action: blinkstick
```
