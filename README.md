
# Autonity Automatic Transaction Challenge

For the Autonity challenge, you are required to send 1000 transactions in less than 30 minutes. The design of this challenge suggests that this task cannot be done manually. Here is a quick workaround using a method that works when you set up another separate wallet on your server and point the key to that wallet for confirming the transactions.

## Instructions:

1. Make the password for the wallet globally accessible by exporting it:

   ```bash
   export 'KEYFILEPWD'=yourpassword
Use the watch command with a 1-second interval to send transactions:

bash
Copy code
watch -n 1 'aut tx make --to YOUR_ADDRESS --value 1 | aut tx sign - | aut tx send -'
Replace yourpassword with the actual password for your wallet and YOUR_ADDRESS with the target address for the transactions.

Note: Ensure that you have the necessary permissions and have set up the Autonity environment correctly before running these commands.

Happy automating!

css
Copy code

Feel free to customize it further based on additional details or context specific to your project or challenge.





