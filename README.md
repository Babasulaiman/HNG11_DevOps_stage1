# User's Management Tool

This bash script automates the creation of user accounts and associated groups based on input from a text file. It is designed for SysOps engineers to efficiently onboard new developers in a secure and organized manner.

## Features

- **User Management:**
  - Creates new user accounts if they do not already exist.
  - Assigns users to their personal group (same name as the username).
  - Adds users to additional groups specified in the input file.

- **Home Directory Setup:**
  - Sets up home directories with appropriate permissions (`700`).

- **Password Generation and Security:**
  - Generates random passwords securely using OpenSSL.
  - Stores passwords in `/var/secure/user_passwords.csv` with restricted permissions (`600`).

- **Logging:**
  - Logs all actions to `/var/log/user_management.log` for auditing and troubleshooting purposes.
  - log file can be easily evoked to verify the script running efficiency.

## Prerequisites

- This script is intended for use on Ubuntu Linux systems.
- Ensure you have administrative privileges (`sudo` access) to execute the script.

## Usage

1. **Clone the repository:**
2. **The script is already executable but can verify**
2. **Provide the script and the name of text file you wish to run the script on**

   ```bash
   https://github.com/Babasulaiman/HNG11_DevOps_stage1.git
   cd HNG11_DevOps_stage1

2. **Prepare the input file:**

- Create a text file (users.txt) containing usernames and their respective groups, formatted as (username;group1,group2.)

    ```bash
    light;sudo,dev,www-data
    idimma;sudo
    mayowa;dev,www-data

3. **Run the script**

    ```bash
    sudo bash create_users.sh users.txt

4. **Verify**

- Check /var/log/user_management.log for detailed logs of the script's execution.
- With the appropraite user check /var/secure/user_passwords.csv for the passwords of the users

5. **Acknowledgement**

- I'm currently taking [https://hng.tech/internship] internship programme.
- This project is Provided by https://hng.tech/internship as stage 1 task.
- Passing this stage means I will be able to move to stage 2 of the devops track during my HNG11 internship.
- Do visit https://hng.tech/hire to know more about HNG.
