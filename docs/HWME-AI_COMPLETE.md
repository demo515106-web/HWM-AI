# HWME-AI Project Documentation

## 1. Project Overview
The HWME-AI project aims to develop a smart home management system leveraging artificial intelligence technologies and IoT protocols for enhanced home automation.

## 2. System Architecture
The architecture consists of:
- A central control unit that processes data and manages commands.
- IoT devices for sensing and actuating (e.g., lights, thermostats).
- Communication protocols such as MQTT for device communication.

## 3. MQTT Topics
The following MQTT topics are used in the system:
- `home/+/temperature`: Used by devices to report temperature data.
- `home/+/command`: For sending commands to devices.
- `home/+/status`: For receiving status updates from devices.

## 4. IR Codes Database
The system supports the following IR codes for controlling devices:
- TV: `0x20DF10EF`
- Air Conditioner: `0x20DF40BF`
- Fan: `0x20DF90A6`

## 5. Commands Reference
The following commands can be issued to devices:
- `power_on`: Turns the device on.
- `power_off`: Turns the device off.
- `set_temperature`: Sets the temperature for HVAC devices.

## 6. Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/demo515106-web/HWM-AI.git
   ```
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Configure the MQTT broker settings in `config.json`.
4. Run the application:
   ```bash
   npm start
   ```

## 7. API Documentation
### Endpoints
- **GET /api/devices**: Retrieves a list of devices.
- **POST /api/devices/:id/command**: Sends a command to a specific device.
### Example Request
```bash
curl -X POST http://localhost:3000/api/devices/1/command -d '{"command":"power_on"}'
```
### Response
```json
{
  "status": "success",
  "message": "Device powered on"
}
```