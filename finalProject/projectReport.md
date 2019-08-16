### Goals Achieved

# Install the 'php' package and create a Puppet module for it
Done, check the team1-puppet repo and 
go to team1-puppet/code/modules/php to view the corresponding Puppet files.

# Install the 'mysql-server' package and create a Puppet module for it
Done, check the team1-puppet repo and 
go to team1-puppet/code/modules/mysql to view the corresponding Puppet files.

# The root page serves index.php rather than index.html
Done, the root page file is now a .php file.

# View registered users from the website
Done, with a caveat. Registered users are displayed as we wanted, but the displayed list also includes some irrelevant information such as programs with special privilges.

# View who is currently logged in
Done, with a caveat. It was rather challenging to show who is currently logged in in a secure way so we opted to display all the users given by using the "last" command. 

# Kick off an account
Abandoned due to security risks involved.

# Lock/unlock an account
Abandoned due to security risks involved.

# Special Notes
We took the security concerns to heart and made changes to our project goals so that there would be less vulnerability risks. This means that no bash commands are sent over the http network, nor are such commands present at the local in the root page file.

Rather than crawling for data using bash commands directly from the .php file, we made use of cron which automatically updates the list of registered users and the list of previously authenticated users, and save the results to a text file. The .php file only needs read the content text files.

The list of registered users is generated with the linux command ```cut -d: -f1 /etc/passwd ```

The list of recent authenticated users is generated with the linux command ```last```
