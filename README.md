# Hello UNIX
Notes to self on how to set up a developer space for myself in MacOS.

This is for setting up a fullstack dev environment for NodeJS, Mongo, and MySQL.

Applications are deployed to Heroku.


### git
0. Open Terminal
1. Enter the `git` command
2. Prompt will appear to install git
3. If not, refer to [https://git-scm.com/](https://git-scm.com/).
4. Set up your github credentials using:
	`git config --global user.name "Your Name && git config --global user.email "you@example.com"`



### ssh
0. Open Terminal
1. Check for any existing SSH keys with `ls -la ~/.ssh`
2. If you get a `No such file or directory` then proceed to step 3, otherwise skip ahead to step 4.
3. Create a new SSH key using `ssh-keygen -t rsa -b 4096 -C "<YOUR EMAIL ADDRESS TIED TO GITHUB>"`
4. Ensure the SSH agent is enabled using `eval "$(ssh-agent -s)"`
5. Add your SSH key using `ssh-add ~/.ssh/id_rsa`
6. Now link the SSH key to github at [https://github.com/settings/keys](https://github.com/settings/keys).
7. In terminal use `pbcopy < ~/.ssh/id_rsa.pub` to get your public key
8. Paste that into Github using the link from step 6.


### NodeJS
0. Open Terminal
1. Navigate to [https://nodejs.org/en](https://nodejs.org/en)
2. Click to download the latest stable (LTS version) of NodeJS
3. After installation, run `node` in Terminal to test if it worked
4. Press `Ctrl C` to exit


### Install Global Node Packages
These are some npm packages I use globally via `sudo npm install -g`

  - chai
  - firebase-tools
  - karma-cli
  - mocha
  - mysql
  - node-debug
  - nodemon
  - sequelize-cli
  - webpack

As an aside, you can view your global packages using `npm list -g --depth 0`


### Homebrew
0. Open Terminal
1. Navigate to [http://brew.sh](http://brew.sh).
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
1. Navigate to [http://dev.mysql.com/downloads/workbench](http://dev.mysql.com/downloads/workbench)
2. Click to download MySQL Workbench
3. After installation, open the Workbench and click "New Connection" to make a Localhost connection


### MongoDB
0. Open Terminal
1. Use Homebrew to install MongoDB using `sudo brew install mongodb` command in Terminal
2. Configure the MongoDB environment using `sudo mkdir -p /data/db/`
3. Get read/write permission using `sudo chown -R $USER /data/db`
4. Test to see if Mongo is working using `mongod` in Terminal


### RoboMongo
1. Navigate to [https://robomongo.org/download](https://robomongo.org/download)
2. Click to download RoboMongo
3. After installation, open RoboMongo and click "New Connection" to make a Localhost connection


### Sublime Text 3
1. Navigate to [https://www.sublimetext.com/3](https://www.sublimetext.com/3)
2. Click to download (no purchase needed)
3. Install the brogrammer syntax highlighting package. In the menu bar click Sublime Text > Preferences > Package Control > Install Package
4. Also install HandlebarsJS and Babel syntax highlighting using the package installer from Step 4
5. Set up other preferences. In the Menu Bar, click Sublime Text > Preferences > Settings. Then, adjust the following properties:

```
{
  "color_scheme": "Packages/Theme - Brogrammer/brogrammer.tmTheme",
  "font_size": 10,
  "ignored_packages":
  [
    "Vintage"
  ],
  "scroll_past_end": true,
  "tab_size": 2,
  "translate_tabs_to_spaces": true
}
```


### Atom (Instead of Sublime Text)
1. Navigate to [https://atom.io/](https://atom.io/)
2. Click to download (it's free)
3. Customization to be continued...


### Heroku CLI
1. Navigate to [Heroku](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up) to review their docs for setting up with NodeJS.
2. Click to install the Heroku CLI for OSX.
3. After installation, run `heroku login` in Terminal.
4. Finally, enter your Heroku account information and boom. Ready.
5. Refer to their `Prepare the app` and `Deploy the app` docs for deployment.



## Optional (For Mobile Development)

### Install Meteor (Web/Mobile Development Framework)
1. Navigate to [https://www.meteor.com/install](https://www.meteor.com/install)
2. Use the `curl` command in Terminal from their website.


### Install Android Studio (for Android App Development)
1. Navigate to [https://developer.android.com/studio/install.html](https://developer.android.com/studio/install.html)
2. Click to install

### Install Xcode (for iOS App Development)
1. Install through the Mac App Store