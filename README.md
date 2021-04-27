[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)  
# Custom YouLess Component for HomeAssistant
Home Assistant custom sensor for YouLess LS120

Based on the version of [Gerben Jongerius](https://bitbucket.org/jongsoftdev/youless) and the aditions of pdwonline.

## Installation
1) Create a folder called `custom_components` if it doesn't exist in your Home Assistant configuration folder
2) Create a folder called `youless` in the `custom_components` folder. 
3) Download all files into this `youless` folder

## Available sensors

 Sensor | Description | Measure
  --- | --- | --- 
  pwr | Current Power usage | W 
  net | Net Power usage | kWh 
  p1 | Power Meter Low | kWh 
  p2 | Power Meter High | kWh 
  n1 | Power Delivery Low | kWh
  n2 | Power Delivery High | kWh
  cs0 | Power Meter Extra | kWh
  ps0 | Current Power usage Extra | W
  gas | Gas consumption | m3


## Configuration example

Add the following configuration under the `sensors:` key in the `configuration.yml` file.

```yaml
  - platform: youless
    name: Youless
    host: <your youless IP address>
    monitored_variables:
      - pwr
      - net
      - p1
      - p2
      - n1
      - n2
      - cs0
      - ps0
      - gas
```
