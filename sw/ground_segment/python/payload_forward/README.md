PAYLOAD
=======

PAYLOAD (downlink) and PAYLOAD_COMMAND (uplink) messages in the pprzlink telemetry act as easy pass-through of information from an autopilot subsystem like a computer vision board to ground station payload control system.

The paparazzi autopilot does not need to understand the data, but just needs to relay it. Payload is typically highly compressed information and only piggy-backs on telemetry when it needs to be transferred over the same long-range low bitrate datalink as the autopilot telemetry.

The PAYLOAD sender (typically a paparazzi module) must make sure the telemetry datalink does not get flooded with payload.


Over the years some standards have developed for payload. One is sending jpeg-thumbnails-chunks. A decoder for this 'jpeg100' is added to the forwarding program.

use ```payload.py --help``` to find currently supported options.
