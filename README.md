# Wokwi-Circuit-design-code
{
  "version": 1,
  "author": "Anonymous maker",
  "editor": "wokwi",
  "parts": [
    { "type": "board-esp32-devkit-c-v4", "id": "esp", "top": 48, "left": 110.44, "attrs": {} },
    { "type": "wokwi-dht22", "id": "dht1", "top": -95.7, "left": 177, "attrs": {} },
    { "type": "wokwi-photoresistor-sensor", "id": "ldr1", "top": 3.2, "left": 346.4, "attrs": {} },
    { "type": "wokwi-potentiometer", "id": "pot1", "top": -135.7, "left": -19.4, "attrs": {} },
    { "type": "wokwi-potentiometer", "id": "pot2", "top": 200.3, "left": -173, "attrs": {} },
    {
      "type": "board-ssd1306",
      "id": "oled1",
      "top": 51.14,
      "left": -182.17,
      "attrs": { "i2cAddress": "0x3c" }
    },
    {
      "type": "wokwi-resistor",
      "id": "r1",
      "top": -63.25,
      "left": 403.2,
      "attrs": { "value": "10000" }
    }
  ],
  "connections": [
    [ "esp:TX", "$serialMonitor:RX", "", [] ],
    [ "esp:RX", "$serialMonitor:TX", "", [] ],
    [ "oled1:VCC", "esp:3V3", "red", [ "v-38.4", "h134.55", "v28.8" ] ],
    [ "oled1:GND", "esp:GND.1", "black", [ "v-48", "h134.4", "v163.2" ] ],
    [ "oled1:SCL", "esp:22", "green", [ "v-57.6", "h259.5", "v48" ] ],
    [ "oled1:SDA", "esp:21", "green", [ "v-67.2", "h259.27", "v105.6" ] ],
    [ "dht1:VCC", "esp:3V3", "red", [ "v0", "h-144" ] ],
    [ "dht1:SDA", "esp:4", "green", [ "v0" ] ],
    [ "dht1:GND", "esp:GND.1", "black", [ "v9.6", "h-201.6", "v153.6" ] ],
    [ "ldr1:VCC", "esp:3V3", "red", [ "h48", "v-48", "h-230.4", "v38.4", "h-220.8" ] ],
    [ "ldr1:GND", "r1:2", "black", [ "h76.8", "v-0.4" ] ],
    [ "r1:1", "esp:GND.1", "green", [ "v-48", "h-316.8", "v307.2" ] ],
    [ "ldr1:DO", "esp:32", "green", [ "h115.2", "v-183", "h-528", "v278.4" ] ],
    [ "pot2:GND", "esp:GND.1", "black", [ "v38.4", "h172.8", "v-124.8", "h48" ] ],
    [ "pot2:VCC", "esp:3V3", "red", [ "v9.6", "h143.2", "v-220.8" ] ],
    [ "pot2:SIG", "esp:32", "green", [ "v19.2", "h182", "v-172.8" ] ],
    [ "pot1:GND", "esp:GND.1", "black", [ "v48", "h48", "v220.8" ] ],
    [ "pot1:VCC", "esp:3V3", "red", [ "v144", "h18.4" ] ],
    [ "pot1:SIG", "esp:35", "green", [ "v201.6", "h-0.4" ] ]
  ],
  "dependencies": {}
}
