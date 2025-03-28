---
title: API - Messaging
---
## Message Structure

| Message Type <br /> 1 Byte <br /> (int8_t)            | Description |
| --------------------------------------------- | ----------- |
|1                                              | Set motor X in Y in direction |
|2                                              | Print sensor X value Y |
|3                                              | Subsystem Wifi Error Message |
|4                                              | Subsystem Wifi Status X |
|5                                              | Subsystem X is not communicating |
|6                                              | Motor Status, X |
|7                                              | Sensor Status, X |
|8                                              | Broadcast |

### Team ID

|  | Alex | Luis | Frank | Tyler | 
|Team Id (char) | 'a' | 'b' | 'c' | 'd'|

### Receiving 

### Message Type 2:

|     | Byte 5 | Byte 6 | Byte 7 |
|------------| --------------| ------------- | ------------- |
| Variable Name | message_type | sensor_id | sensor_value |
|Variable Type | int8_t | char | int8_t |
| Min Value| 1 | 1 | 0 |
| Max Value| 8 | 2 | 100 |
| Example | 2 | 2 | 50 |

### Message Type 5:

|      | Byte 5 | Byte 6 |
|------------| --------------| ------------- |
| Variable Name | message_type | subsystem_id |
|Variable Type | int8_t | char |
| Min Value | 1 | a |
| Max Value| 8 | d |
| Example | 5 | c |

### Message Type 6:

|      | Byte 5 | Byte 6 |
|------------| --------------| ------------- |
| Variable Name | message_type | motor_status |
|Variable Type | int8_t | uint8_t |
| Min Value | 1 | 0 |
| Max Value| 8 | 1 |
| Example | 6 | 0 |

### Message Type 7:

|      | Byte 5 | Byte 6 |
|------------| --------------| ------------- |
| Variable Name | message_type | sensor_status |
|Variable Type | int8_t | uint8_t |
| Min Value | 1 | 0 |
| Max Value| 8 | 1 |
| Example | 7 | 0 |

### Sending

### Message Type 1:

|   | Byte 5 | Byte 6 | Byte 7 |
|------------| --------------| ------------- | ------------- |
| Variable Name | message_type | motor_id | motor_direction |
|Variable Type | int8_t | char | char |
| Min Value| 1 | 1 | 0 |
| Max Value| 8 | 3 | 2 |
| Example | 1 | 2 | 1 |

### Message Type 3:

|      | Byte 5 | Byte 6 - Byte 55 |
|------------| --------------| ------------- |
| Variable Name | message_type | error_message |
|Variable Type | int8_t | char |
| Min Value| 1 | Wifi not connecting |
| Max Value| 8 | Wifi is connecting |
| Example | 3 | Wifi is connecting |

### Message Type 4:

|      | Byte 5 | Byte 6 |
|------------| --------------| ------------- |
| Variable Name | message_type | wifi_status |
|Variable Type | int8_t | char |
| Min Value | 1 | 0 |
| Max Value| 8 | 1 |
| Example | 4 | 0 |

### Broadcast

### Message Type 8:

|      | Byte 5 | Byte 6 - Byte 55 |
|------------| --------------| ------------- |
| Variable Name | message_type | broadcast_message |
|Variable Type | int8_t | char |
| Min Value| 1 | Minimum value is 1 character |
| Max Value| 8 | Max value is 48 characters |
| Example | 8 | This is broadcast |
