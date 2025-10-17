# What are we building?

## Hardware
- Arduino
  - GPS module
- Physical compass
- LED ring to surround compass

## Programming languages
- C++

## Features

### Gieger counter
Two modes:
- **Lock-on mode**: Tick rate dependent upon only the distance to the nearest pub
- **Density mode**: Tick rate dependent on distance to all nearby pubs - becomes a metric of nearby pub density

A button switches between the two.


### Compass
The user uses the physical compass on the device to point the device to north. The device then provides a bearing to the nearest pub.

**Stretch goal**: a needle that points towards the nearest pub
- Would require an orientation input, which would be an additional arduino module

### No internet connectivity
- We do not want the device to be dependent upon wifi/5g signal. Only external data source is GPS.

## Inputs
- **Pub locations**
  - From OpenStreetMap.
  - Ideally would be able to load a whole country's data at once. At a minimum, want at least a city/region's data on the device.
  - Data loaded from personal computer before using.
- **Device location**
  - GPS data from arduino GPS module

## Outputs
- LED ring -> bearing angle
- Speaker -> geiger counter counts