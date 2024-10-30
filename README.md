# Security Configuration Files

## Dynamic Password Implementation for Project Security

### Description

These files contain code to add a dynamic password for enhancing the security of your project. The password is stored in EEPROM so that it is not erased when the program is closed.

### Configuration Options

- **Maximum Login Attempts:** Set to `3` (defined by `Tries_Max`).
- **Username Requirements:** Minimum length of `7` characters (defined by `USERNAME_MIN_LENGTH`).
- **Password Requirements:** Minimum length of `5` characters (defined by `PASSWORD_MIN_LENGTH`).

### Input and Output Configuration

- **Output Options:**
  - `CLCD_OUTPUT`
  - `TERMINAL_OUTPUT`
  
  The output type is defined by the `OUTPUT_SCREEN` macro.

- **Input Options:**
  - `KPD_INPUT`
  - `TERMINAL_INPUT`
  
  The input type is defined by the `INPUT_DATA` macro.

### Function Mapping

  - You can specify function names used for interacting with different modules in your project:
  - If the function names in your drivers are not the same as the function names in my drivers, all you need to do is change the function names of the macros in the config.h file, and then the code will work perfectly for you.


### Usage Instructions

1. **Initialize EEPROM:**
   - Retrieve the username and password length from EEPROM.
   - Load the number of remaining login attempts.

2. **User Registration:**
   - If no username is found, prompt the user to set one up.
   - Validate the username based on minimum length requirements.

3. **Security Features:**
   - Lock the user out after exceeding the maximum number of attempts.
   - Store the username and password securely in EEPROM for future logins.

### Conclusion

Make sure to adjust the configuration file to meet the needs of your project, and define the necessary input/output methods and function mappings to suit your hardware setup.
