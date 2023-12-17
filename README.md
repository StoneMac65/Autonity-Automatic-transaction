# Autonity-Automatic-Transaction

This repository is dedicated to solving the Autonity challenge of sending 1000 transactions in less than 30 minutes. The design of this challenge indicates that manual execution is not feasible. The following method provides a workaround. Note that this method assumes you have set up another separate wallet in your server.

## Quick Start

1. Make the password for the wallet globally accessible:

   
    export 'KEYFILEPWD'=yourpassword
    
2. Use the watch command with a 1-second interval to send transactions:

   
    watch -n 1 'aut tx make --to YOUR ADDRESS --value 1 | aut tx sign - | aut tx send -'
    
Replace yourpassword with the actual password and YOUR ADDRESS with the recipient's address.

This method leverages the watch command to automate the transaction sending process.

Note: Ensure that you have the necessary permissions and configurations set up before executing these commands.

For more details on Autonity, refer to their official documentation.
