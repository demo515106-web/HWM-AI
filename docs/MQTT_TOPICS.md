# MQTT Topics Documentation

This document provides a comprehensive overview of the MQTT topics used in the project.

## Topic Structure

The topics are structured hierarchically to reflect the organization and functionality.  They adhere to the following format:

```
<base_topic>/<sub_topic1>/<sub_topic2>/...
```

## Listed Topics

1. **home/sensors/temperature** - Temperature readings from various sensors.
2. **home/sensors/humidity** - Humidity readings.
3. **home/actuators/lights** - Control topics for lighting systems.
4. **home/notifications/** - General notifications sent to the home system.

### Usage Examples
- To subscribe to temperature updates, use the topic: `home/sensors/temperature`
- To send a command to turn on lights, publish to: `home/actuators/lights/on`

## Conclusion

This documentation should help developers easily understand and implement MQTT communications within the project.