# Create and use LAMP stack to make a user management dashboard

## concrete goals for your project, and methods of testing and verification you will apply to determine whether those goals were met

- In addition to the already installed Apache2 package, the following will be achieved to complete the entire project.

- Install the package for PHP, and create a Puppet module to set package persistence and configuration property

- Install the package for MySql, and create a Puppet module to set up proper configuration

- Configure the web server so that the /var/www/html directory serves from index.php rather than index.html

- Write some PHP code to implement a few functionalities including,
    - Currently registered users in the system and the group they belong to
    - Who is currently logged in
    - Kick off an account
    - Lock/unlock an account

- Testing will be conducted by creating dummy users that log into our server. We will be testing if we are able to kick off and disable and enable their accounts. 

- If we are able to run the server based on a PHP file and can display and perform the aforementioned user management functionalities, then the project is completed.

##	a discussion of your project's effect on its user population, and the user support issues it might raise
- I don’t think this project has any direct effects on its user population, because a user management dashboard is supposed to be used and handled by a system administrator. 
- Users might be annoyed when their actions incur a freeze on their account. 

##	a discussion of security issues relevant to your project
- Sending bash commands over http is a huge security risk in any other regular web development environment, should we make our web server SSL certified?

##	a discussion of the work needed to complete the project and what might be needed to maintain it for continued future use, and ways that installation and maintenance tasks can be automated
- In order to complete the project we have to install the necessary dependencies and create the necessary Puppet configurations.
- Things that are considered for maintaining the project include keeping the packages up to date, fix any of the updates that may have conflicts with the build.
- Dependency upgrades could be automated using Puppet.

##	documentation of the project, both for the system administration work involved and for your user community
- Contributors and project description (to be completed as we begin working)
- How to use (for other sysadmins) (to be completed as we begin working)

