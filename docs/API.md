---
title: API - Messaging
---
## Message Structure

| Message Type <br /> 1 Byte <br /> (int8_t)            | Description |
| --------------------------------------------- | ----------- |
|1                                              | Set motor in X position |
|2                                              | Print sensor value, X |
|3                                              | Set target RPM, X |
|4                                              | Broadcast |

### Team ID

|  | Alex | Luis | Tyler | Frank |
|--|------|------|-------|-------|
|Team Id (char) | a | b | c | d |

## Receiving

### Message Type 2:

|     | Byte 5 | Byte 6 |
|------------| --------------| ------------- |
| Variable Name | message_type | sensor_value |
|Variable Type | int8_t | int8_t |
| Min Value| 2 | 0 |
| Max Value| 2 | 100 |
| Example | 2 | 50 |

## Sending

### Message Type 1:

|   | Byte 5 | Byte 6 |
|------------| --------------| ------------- |
| Variable Name | message_type | motor_direction |
|Variable Type | int8_t | int8_t |
| Min Value| x01 | x00 |
| Max Value| x01 | x02 |
| Example | x01  | x01 |

### Message Type 3:

|     | Byte 5 | Byte 6 |
|------------| --------------| ------------- |
| Variable Name | message_type | sensor_target |
|Variable Type | int8_t | int8_t |
| Min Value| x03 | 0 |
| Max Value| x03 | 100 |
| Example | x03 | 50 |

## Broadcast

### Message Type 4:

|      | Byte 5 | Byte 6 - Byte 55 |
|------------| --------------| ------------- |
| Variable Name | message_type | broadcast_message |
|Variable Type | int8_t | string |
| Min Value| x04 | Minimum value is 1 character |
| Max Value| x04 | Max value is 48 characters |
| Example | x04 | This is broadcast |

## Message Code Key

### Message Type 1

|  Value | Key / Meaning|
|--------|--------------|
| 0 | closes gate |
| 1 | opens gate fully |
| 2 | Gate is half open/closed |

## Code

<br>Here is the [code](./subfolder/code_esp32_mqtt.zip) to test functionality of system.
