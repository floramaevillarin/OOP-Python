# Project Structure

The project is divided into three main modules:

- **`users.py`**
- **`theDevices.py`**
- **`main.py`**

Additionally, two supporting files are used:
- **`users.pkl`**: Stores user authentication data.
- **`devices.txt`**: Contains information about devices.

## Components Overview

### 1. `User` Class (`users.py`)
Handles user authentication and login processes.

- **Initialization**:  
  Initializes user data from the `users.pkl` file and sets the default login attempts to 3.

- **Load Users**:  
  `load_users(self)` loads user data from the `users.pkl` file.

- **Login**:  
  `login(self)` verifies the username and password, allowing a maximum of 3 attempts.

- **Register User**:  
  `register_user(self)` registers a new user and saves their credentials.

- **Save Users**:  
  `save_users(self)` saves user credentials to the `users.pkl` file.

> **Note**: Default credentials are `username: admin` and `password: Pyth0n2023`.

---

### 2. `DeviceManagement` Class (`theDevices.py`)
Manages device-related operations, including viewing, adding, updating, deleting, and searching for devices.

- **Initialization**:  
  Loads device data from the `devices.txt` file.

- **Load Devices**:  
  `load_devices(self)` loads the list of devices from `devices.txt`.

- **Save Devices**:  
  `save_device(self)` saves the updated device list back to `devices.txt`.

- **View Devices**:  
  `view_devices(self)` displays all devices.

- **Add Device**:  
  `add_device(self, name)` adds a new device if it doesn't already exist.

- **Delete Device**:  
  `delete_device(self, device_to_delete)` deletes a device based on its code.

- **Update Device**:  
  `update_device(self, device_to_update, new_name)` updates a device's name.

- **Validate Device**:  
  `validate_device(self, old_name)` checks if a device exists in `devices.txt`.

- **Search Devices**:  
  `search_device(self, keyword)` searches for devices containing the specified keyword.

- **Device Menu**:  
  `main_menu(self)` displays a menu for managing devices and executing user-selected actions.

---

### 3. Main Function (`main.py`)
The main function drives user interaction. It initializes the `User` and `DeviceManagement` classes. Upon successful user login, the device management menu is presented, allowing users to perform various actions on devices.

---

