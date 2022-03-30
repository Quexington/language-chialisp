# language-Chialisp
Support for [Chialisp](https://chialisp.com/) syntax highlighting with Atom's default "one-dark-syntax" highlighter.

You can install this package through the atom package installer or by placing it manually into your ~/.atom/packages directory and running `apm i` from within the project directory.

Contributions are very welcome!  I threw this together pretty quickly and have never made one before so I'm 100% positive there are improvements to be made.

## Older MacOS versions
Some older version of MacOS don't have the required tools to build this package in Atom.  Follow the instructions below (https://medium.com/@mrjohnkilonzi/how-to-resolve-no-xcode-or-clt-version-detected-d0cf2b10a750) to install the necessary tools to build this.

Step 1: Find the path to the Command Line Tools for Xcode

```
xcode-select -print-path
/Library/Developer/CommandLineTools #This is the output, is no output the Xcode is not installed. We need to install it Skip to Step 6
```

Step 2: Reset the path of Command Line Tools for Xcode

```
sudo xcode-select --reset
```

Step 3: Check if the path has been reset

```
xcode-select -print-path
/Applications/Xcode.app/Contents/Developer #If this is the output then everything is fine. Restart your Mac just to be sure. If nothing changes come back here and continue with the steps
```

Step 4: Uninstall whatever is left of the Command Line Tools for Xcode

```
sudo rm -rf $(xcode-select -print-path) #There will be no output
sudo rm -rf /Library/Developer/CommandLineTool #Just to be sure
```

Step 5: Install Command Line Tools for Xcode

```
xcode-select --install
```

