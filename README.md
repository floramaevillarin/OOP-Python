Project Structure
The codebase is divided into three primary components:

users.py
theDevices.py
main.py
Each component plays a vital role in the application's functionality. Additionally, two supporting files are included:

users.pkl: Stores user authentication data.
devices.txt: Contains information about devices.
Components Overview
1. User Class (users.py)
This class manages user authentication, including login attempts and user registration.

Initialization:
The __init__(self) method loads user data from the users.pkl file and sets a default of 3 login attempts.

Load:
load_users(self) loads user data from the users.pkl file.

Login:
login(self) allows users to input their username and password, verifying credentials against the data in users.pkl. It also enforces a 3-attempt limit.

Register:
register_user(self) registers a new user by saving their credentials to the file.

Save User:
save_users(self) saves the user credentials to the users.pkl file.

Note: The default admin credentials are username: admin and password: Pyth0n2023.

2. DeviceManagement Class (theDevices.py)
This class manages device-related operations, including viewing, adding, updating, deleting, and searching for devices.

Initialization:
The __init__(self) method initializes the device list by loading data from devices.txt.

Load:
load_devices(self) loads devices from the devices.txt file.

Save:
save_device(self) saves the updated list of devices back to devices.txt.

View:
view_devices(self) displays all devices currently in the list.

Add:
add_device(self, name) adds a new device if it doesn't already exist.

Delete:
delete_device(self, device_to_delete) removes a device from the list based on the provided code.

Update:
update_device(self, device_to_update, new_name) updates a device's name from device_to_update to new_name.

Validate:
validate_device(self, old_name) verifies whether a device exists in devices.txt.

Search:
search_device(self, keyword) searches for devices that match a given keyword.

Menu:
main_menu(self) displays a menu of device management options, processes user input, and executes the corresponding action.

3. Main Function (main.py)
The main.py script orchestrates user interaction. It initializes instances of the User and DeviceManagement classes. Once the user successfully logs in, the device management menu is presented for further actions.
