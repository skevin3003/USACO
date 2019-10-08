# C++ 

## Command Line (Mac)

Follow the instructions [here](https://wiki.helsinki.fi/display/HUGG/GNU+compiler+install+on+Mac+OS+X?fbclid=IwAR3bnM6A_kTgXD2p5nOfVbxRRQ4nHMj89jllNy1-zdtfXfcq1czbSoXiWgE). Step 4 might give errors but it should still install. After this, running the following command should display gcc.

```
gcc --version
```

The following command should also work.

```
brew install gcc
```

In this case, the g++ command will still default to clang, but you can substitute g++-8 instead.

## Shortcuts

Open your bash profile with a text editor such as gedit.

```
brew install gedit
gedit ~/.bash_profile
```

Add the following functions.

```
co() { 
    g++ -std=c++17 -Ofast -Wall -Wl,-stack_size -Wl,0x10000000 -o $1 $1.cpp
}
run() {
    co $1 && ./$1
}
```

Now you can easily run C++ from the command line by calling run.

```
run [prog name]
```

## Troubleshooting

Make sure you have installed XCode command line tools.

```
xcode-select --install
xcode-select --version
softwareupdate --list
softwareupdate -i -a
```

For OS X Mojave, navigate to your bash profile
```
gedit ~/.bash_profile
```
and add the following line:
```
export CPLUS_INCLUDE_PATH="/usr/local/include/c++/8.1.0/:/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.14.sdk/usr/include:$CPLUS_INCLUDE_PATH"
```

## IDE 

### Online

* [CSAcademy](https://csacademy.com/workspace/)
	* I use this the most. it is the best one
* [Ideone](http://ideone.com/)
* [Cloud9](https://c9.io/)

### Local

 * [Sublime Text 3](https://www.sublimetext.com/)
   * [Editing Build Settings](https://stackoverflow.com/questions/23789410/how-to-edit-sublime-text-build-settings)
   * [FastOlympicCoding Addon](https://github.com/Jatana/FastOlympicCoding)
 * [Geany](https://www.geany.org/)
 * [Visual Studio Code](https://code.visualstudio.com/)
 * [XCode](https://developer.apple.com/xcode/)
   * mac
 * [Codeblocks](http://www.codeblocks.org/)
   * bad on mac :(


## Useful Links

### Reference

* [cplusplus](http://www.cplusplus.com/reference/)
* [cppreference](http://en.cppreference.com/w/)

### Other

 * [Intro to Command Line](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line)
 * [Command Line Shortcuts](https://jonsuh.com/blog/bash-command-line-shortcuts/)
 * [Run Python Script](https://stackoverflow.com/questions/7855996/cant-run-python-py-files-from-terminal-on-mac)
 * [Competitive C++ Style Guide](https://codeforces.com/blog/entry/64218)
