# Hello Mac
Notes to Self on How to Set Up a developer space for myself in MacOS.


### git
0. Open Terminal
1. Enter the `git` command
2. Prompt will appear to install git
3. If not, refer to (https://git-scm.com/)[https://git-scm.com/].


### ssh
0. Open Terminal
1. Check for any existing SSH keys with `ls -la ~/.ssh`
2. If you get a `No such file or directory` then proceed to step 3, otherwise skip ahead to step 4.
3. Create a new SSH key using `ssh-keygen -t rsa -b 4096 -C "<YOUR EMAIL ADDRESS TIED TO GITHUB>"`
4. Ensure the SSH agent is enabled using `eval "$(ssh-agent -s)"`
5. Add your SSH key using `ssh-add ~/.ssh/id_rsa`
6. Now link the SSH key to github at (https://github.com/settings/keys)[https://github.com/settings/keys].
7. In terminal use `pbcopy < ~/.ssh/id_rsa.pub` to get your public key
8. Paste that into Github using the link from step 6.


### NodeJS
0. Open Terminal
1. Navigate to (https://nodejs.org/en)[https://nodejs.org/en]
2. Click to download the latest stable (LTS version) of NodeJS
3. After installation, run `node` in Terminal to test if it worked
4. Press `Ctrl C` to exit


### Homebrew
0. Open Terminal
1. Navigate to (http://brew.sh)[http://brew.sh].
2. Copy the command on their website into Terminal and run it
3. Press the Enter key to confirm the download to the default folder
4. Enter the `brew` command after the download to confirm it worked


### MySQL
0. Open Terminal
1. Use Homebrew to install MySQL using `sudo brew install mysql` command in Terminal
2. Run the MySQL server after the installation is complete by entering `mysql.server start` in Terminal
3. Test if the server is working by entering `mysql -u root` 
4. Type `\q` in Terminal to exit the MySQL CLI


### MySQL Workbench
1. Navigate to (http://dev.mysql.com/downloads/workbench)[http://dev.mysql.com/downloads/workbench]
2. Click to download MySQL Workbench
3. After installation, open the Workbench and click "New Connection" to make a Localhost connection


### MongoDB
0. Open Terminal
1. Use Homebrew to install MongoDB using `sudo brew install mongodb` command in Terminal
2. Configure the MongoDB environment using `sudo mkdir -p /data/db/`
3. Get read/write permission using `sudo chown -R $USER /data/db`
4. Test to see if Mongo is working using `mongod` in Terminal


### RoboMongo
1. Navigate to (https://robomongo.org/download)[https://robomongo.org/download]
2. Click to download RoboMongo
3. After installation, open RoboMongo and click "New Connection" to make a Localhost connection


### Sublime Text 3
1. Navigate to (https://www.sublimetext.com/3)[https://www.sublimetext.com/3]
2. Click to download (no purchase needed)



