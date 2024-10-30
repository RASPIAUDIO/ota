
Firmware Over-The-Air Tools
===========================

## How-to-OTA (Ubuntu/Arduino)

First find out the link to "sketch.bin" (in the logs when uploading the sketch)

(Something like this => /tmp/arduino_build_810145/sketch.ino.bin)

Then


```bash
cp sketch.bin ~/Arduino/libraries/ArduinoIoTCloud/extras/tools/
cd ~/Arduino/libraries/ArduinoIoTCloud/extras/tools
./lzss.py --encode sketch.bin sketch.lzss
./bin2ota.py ESP32 sketch.lzss sketch.ota
```

