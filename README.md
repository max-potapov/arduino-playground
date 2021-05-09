# Arduino Playground
Playing with Arduino UNO on MacOS via Visual Studio Code

## Installing tools
1. `brew install arduino-cli # use "--build-from-source" for Apple Silicon`
2. `arduino-cli core update-index`
3. `arduino-cli core install arduino:avr`

## vscode-arduino configurations
`arduino.json`
```json
{
    "sketch": "Blink.ino",
    "port": "/dev/cu.usbserial-142220", 
    "configuration": "cpu=atmega328",
    "board": "arduino:avr:uno",
    "programmer": "avrispmkii"
}
```
* look for a port from `arduino-cli board list` output

`settings.json`
```json
{
    "arduino.additionalUrls": "",
    "arduino.useArduinoCli": true,
    "arduino.enableUSBDetection": true,
    "arduino.path": "/usr/local/bin",
    "arduino.commandPath": "arduino-cli"
}
```
* find a path with `which arduino-cli`
