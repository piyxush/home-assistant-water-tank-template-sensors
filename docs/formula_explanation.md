# Formula Explanation

## Water Volume

The volume formula converts the ultrasonic sensor reading into liters.

### Formula
`Volume = 2000 - (distance × 1700)`

### Meaning
- `2000` is the reference tank capacity or calibration constant
- `distance` is the ultrasonic sensor reading
- `1700` is the scaling factor used for conversion

## Water Level Percentage

### Formula
`Level % = ((110 - (distance × 100)) × 1.1112)`

### Meaning
- `110` is a calibration reference value
- `100` is a unit conversion factor
- `1.1112` is a scaling constant used to map the reading to percentage

## Important

These constants are calibration-specific. They must be adjusted for your tank dimensions and sensor placement.