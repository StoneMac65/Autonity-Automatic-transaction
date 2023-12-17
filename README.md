# Autonity-Automatic-transaction
for new autonity challenge you need to send 1000 transactions in less than 30 minutes
the design of this challenge suggests that this task can not be done manually
so here is the quick work around
this method only works if you set another seperate wallet in your server and point the key to that wallet for confirming the transactions


#first need to make the password for the wallet globally accessible 

export  'KEYFILEPWD'= yourpassword

#then use the simple watch command with 1 second interval to send transaction

watch -n 1 'aut tx make --to YOUR ADDRESS  --value 1 | aut tx sign - | aut tx send -'
