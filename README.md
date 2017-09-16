# Hello UNIX
Notes to self on how to set up a developer space for myself in MacOS.

This is for setting up a fullstack dev environment for NodeJS, Mongo, and MySQL.
Python coming soon!

Applications are deployed to Heroku.


### git
0. Open Terminal
1. Enter the `git` command
2. Prompt will appear to install git
3. If not, refer to [https://git-scm.com/](https://git-scm.com/).
4. Set up your github credentials using:
	`git config --global user.name "Your Name && git config --global user.email "you@example.com"`



### Unhide the /Library Folder
0. Run `chflags nohidden ~/Library/` in Terminal


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


### Python
Note that Python 2 is usually installed in Mac OS out of the box

0. Open Terminal
1. Check for Python version by typing `python`

If you have Python 2, and want to keep it that way that's cool

0. Note that you may also want to intall the pip package manager for Python 2 using `sudo easy_install pip`
1. You can test if it installed and get the version with `pip -V`

If you want Python 3, then you can install that and pip3 in one shot 

0. Assuming Homebrew is installed, enter `brew install python3` to get Python 3
1. You can test if Python 3 installed and get the version with `python3 -V`
2. You can test if pip installed and get the version with `pip3 -V`


### Anaconda (for data science in Python)
You can also use [Canopy](https://www.enthought.com/products/canopy/) instead of [Anaconda](https://www.continuum.io/downloads). But I picked Anaconda so I can pick either Python 2 or 3.

Note! If you did all the installations I mentioned in this repo, then you will have 3 Python versions on your Mac. One shy of [this guy](http://stackoverflow.com/questions/33541876/os-x-deciding-between-anaconda-and-homebrew-python-environments). This shouldn't be an issue but it's good to be aware of it. I plan on using the Mac and Homebrew verisons for web development and the Anaconda version for Data Science.

Anyway, install Anaconda by doing the following:

0. On the [Anaconda](https://www.continuum.io/downloads) website choose either the Python 2 or Python 3 version.
1. I picked the Graphical Installer (green button) for Python 3.6.
2. Follow along with the installer's instructions.
3. Type `conda` in your command line to ensure the download was successful.
4. You can look into this [GitHub Repo](https://github.com/brandon-rhodes/pycon-pandas-tutorial) to mess with the Pandas library in Python.

Note that [Jupyter](http://jupyter.readthedocs.io/en/latest/install.html) should come with Anaconda. If not, use their instructions to download it. Using  `pip` or `pip3` is the easiest download. Type `jupyter` in the command line to see if it was installed.


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
5. Add the `subl` command to your path using the directions in [this repo](https://stackoverflow.com/questions/16199581/open-sublime-text-from-terminal-in-macos).
6. Set up other preferences. In the Menu Bar, click Sublime Text > Preferences > Settings. Then, adjust the following properties:

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
3. Customization to be continued.


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
3. Refer to the [React Native Docs](https://facebook.github.io/react-native/docs/getting-started.html) to set up Andriod to work with React Native.
4. Set the environmental variable in Terminal by typing `nano ~/.bash_profile` and then pasting in...
```
export ANDROID_HOME=~/Library/Android/sdk
export PATH=${PATH}:${ANDROID_HOME}/tools
export PATH=${PATH}:${ANDROID_HOME}/platform-tools
```
5. Then, save your changes by typing `ctrl+o`. Hit `return` to save. Then exit Nano by typing `ctrl+x`.
6. Activate your changes in Terminal with `source .bash_profile`. Refer to [this](https://natelandau.com/my-mac-osx-bash_profile/), [this](http://stackoverflow.com/questions/28296237/set-android-home-environment-variable-in-mac), and [this](http://stackoverflow.com/questions/19986214/setting-android-home-enviromental-variable-on-mac-os-x) for more info.

7. Fire up the Andriod Emulator with `andriod avd` in Terminal.


### Install Android File Transfer
1. Navigate to [https://www.android.com/filetransfer/](https://www.android.com/filetransfer/)
2. Follow download instructions
3. Use this to copy apps to your device directly


### Install Java Development Kit (JDK)
1. Navigate to [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) and download the OSX version
2. Then open Terminal and input `brew install android-sdk` (uses Homebrew)
3. After the download, input `andriod` into Terminal to open the Andriod SDK
4. Refer to the [Facebook Docs](http://facebook.github.io/react-native/docs/getting-started.html) to determine the SDK Packages to install


### Install Maven (for Java Web Development)
1. Open Terminal and run `brew install maven` (uses Homebrew)
2. Run `mvn -v` to ensure the download was complete


### Install IntelliJ (for Java Web Development)
1. Navigate to [Jetbrains IDEA](https://www.jetbrains.com/idea/#chooseYourEdition) to download the community edition.
2. Leave the default setting during installation.
3. Opening IntelliJ for the first time, you may need to point the Project SDK to your previously downloaded Java 8 JDK. Using the folder selector, your JDK should be located at /Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home


### Install Xcode (for iOS App Development)
1. Install through the Mac App Store


### React Native
1. Note you will follow the next steps only after downloading Xcode for iOS development and/or downloading Andriod with Java for Andriod development
2. In Terminal, run `sudo npm install –g react-native-cli`
3. Also in Terminal, run `sudo npm install -g rninit`


## Very Optional (Just Because)

### Install Wordpress
1. Navigate to [https://serverpress.com](https://serverpress.com)
2. Click on the Free Download


### Install dotnet (for .NET Development)
1. Open Terminal and run `brew cask install dotnet` (uses Homebrew)
2. Run `dotnet --version` to ensure the download was complete
3. You may also need to install the dotnet SDK from (here)[https://www.microsoft.com/net/core#macos]
4. Once the SDK is installed, you can try step 2 again.


### Install Visual Studio IDE (for .NET Development)
1. Visit [https://www.visualstudio.com/](https://www.visualstudio.com/) for the download