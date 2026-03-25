# Home Assistant Water Tank Template Sensors

This repository contains Home Assistant template sensors for monitoring an overhead water tank using an ultrasonic sensor.

## Features

- Calculates total water volume in liters
- Calculates water level in percentage
- Built for Home Assistant template sensors
- Uses Jinja2 expressions inside YAML configuration

## How it works

The sensors take the distance reading from an ultrasonic sensor and convert it into:

- **Water volume (L)**
- **Water level (%)**

## Example sensors

- `Total Water Volume`
- `Overhead Water Level`

## Requirements

- Home Assistant
- A working ultrasonic distance sensor entity
- Template sensor support in Home Assistant

## Configuration

Add the YAML file to your Home Assistant configuration.

### Water volume sensor
```yaml
template:
  - sensor:
      - name: "Total Water Volume"
        unit_of_measurement: "L"
        default_entity_id: sensor.overhead_water_volume
        state: "{{ (2000 - (states('sensor.esphome_web_cfdefc_ultrasonic_sensor') | float(0) * 1700)) | round(0) }}"
