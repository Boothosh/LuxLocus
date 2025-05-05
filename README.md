# LuxLocus

## ℹ️ About

LuxLocus is a project targeting to develop an indoor location tracking system wich provides 3D locations for a given beacon relativ to four or more anchors.

## Abstraction

The LuxLocus system consists out of one or more beacons, four or more anchors and one master. On start up the master communicates with the targets a unique frequency, which they shall use for further communication. Once that's set up, every target blinks periodically on that frequency. The anchors receive this blink impulse and transmit this measurement event to the master. Knowing the delays, with wich the anchors received the beacons signal, the master can reconstruct the spatial location of the beacon.

### Disclaimers

- The four anchors shouln't lay in one level.
- If you are using only four anchors, two possible locations will be computed by the master.
- The postion of the anchors has to be known to the master.
- The transmittion time of signal-reception-events by the anchors to the master has to be the same for all anchors or they have to have a syncronized clock.
