# Security Configuration Files

## Dynamic Password Implementation for Project Security

### Description

These files add a dynamic password to boost project security. The password is stored in EEPROM to retain settings even after closing the program.

### Configuration Options

- **Maximum Login Attempts:** `3` (defined by `Tries_Max`).
- **Username Requirements:** Minimum `7` characters (defined by `USERNAME_MIN_LENGTH`).
- **Password Requirements:** Minimum `5` characters (defined by `PASSWORD_MIN_LENGTH`).

### Input and Output Configuration

- **Output Options:**
  - `CLCD_OUTPUT`
  - `TERMINAL_OUTPUT`
  
  Configure the output type using the `OUTPUT_SCREEN` macro.

- **Input Options:**
  - `KPD_INPUT`
  - `TERMINAL_INPUT`
  
  Set the input type through the `INPUT_DATA` macro.

### Function Mapping

If your function names differ, simply update the macros in the config.h file to match your module functions. This will ensure compatibility with your project’s drivers.

### Usage Instructions

1. **Initialize EEPROM:**
   - Retrieve username and password length from EEPROM.
   - Load remaining login attempts.

2. **User Registration:**
   - If no username exists, prompt the user to set one.
   - Ensure the username meets the length requirement.

3. **Security Features:**
   - Lock the user out after exceeding maximum attempts.
   - Securely store username and password in EEPROM.

## Testing
You can find testing details for these files in the repository: [Advanced-Safe](https://github.com/abdallah-shehawey/Advanced-Safe.git)

## Resources for Use and Adaptation
You may refer to [this LinkedIn post](https://www.linkedin.com/posts/abdallah-shehawey_embeddedsystems-microcontroller-atmega32-activity-7257827462447857664-sBEJ?utm_source=share&utm_medium=member_desktop) for further insights on using and adapting these files for your specific setup.
