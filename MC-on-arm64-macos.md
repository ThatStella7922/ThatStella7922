# Minecraft on arm64 macOS (M1, M1 Pro, M1 Max)
### by ThatsNiceGuy

This guide will help you to install Minecraft on your arm64 Mac and have it run fully natively.
This guide was written and tested on a MacBook Pro 14" (M1 Max 10c/32c, 32GB RAM, 1TB SSD). Should work on all M1 machines.

## Getting Java installed
First things first, you need some Java. 

Head over to [Adoptium's website](https://adoptium.net/releases.html), then select `macOS` for `Operating System` and then select `aarch64` for Architecture.

It should look like this:

<img width="1069" alt="image" src="https://user-images.githubusercontent.com/10524728/141716886-6b17408a-5e96-4199-9fff-fe8a47bf951b.png">
Download the `.pkg` variant, then install it.

## Registering Java
### Part 1
Open up a Terminal and enter `cat .zshrc`. If you see an error that says `cat: .zshrc: No such file or directory` then continue to part 2. If you see some "code" then skip to part 3.

### Part 2
In your Terminal, enter `touch .zshrc`.

### Part 3
open Finder and click Go -> Home from the menu bar. Now press ⌘⇧. (Command + Shift + .) to show hidden files. Open the file called `.zshrc` and put in the following:
```JAVA_HOME="/Library/Java/JavaVirtualMachines/temurin-17.jdk/Contents/Home"```

It should look like this:

<img width="567" alt="image" src="https://user-images.githubusercontent.com/10524728/141717781-cb93d7a7-9718-43b9-94d5-f28524d3d8c2.png">

Now save it and close TextEdit.


## Installing Minecraft
### Downloading the wrapper
Go to [https://github.com/yusefnapora/m1-multimc-hack](https://github.com/yusefnapora/m1-multimc-hack) and click the green 'Code' button then 'Download ZIP'. Extract it then put the entire folder on your desktop.

Now open Finder and click Go -> Home from the menu bar to open your home folder again. Create a new folder there called `Minecraft` and move the `m1-multimc-hack` folder from your Desktop to inside the Minecraft folder.

<img width="549" alt="image" src="https://user-images.githubusercontent.com/10524728/141718752-70ebe854-4d85-4664-b37e-23a949467a53.png">
This is how it should look like with Finder's columns view.

### MultiMC setup
Go to [multimc.org](http://multimc.org) and download MultiMC for Mac.

Open it and it will ask for your java installation.

<img width="383" alt="image" src="https://user-images.githubusercontent.com/10524728/141718196-2c64fb87-dcaa-4635-96a1-65fdeae42d90.png">
It will look like this. Choose either one.

Now open your Terminal and type in `echo $PWD`. You will see an output like this: `/Users/thatsniceguy`. The name after the `/Users/` part is your Mac username. in this example, mine is `thatsniceguy`. Take note of it.

Make sure to login to your Minecraft account (log in like normal in MultiMC).

Now open MultiMC's settings and go to the Custom Commands. Where it says `Wrapper`, paste in the following:\
```/Users/<your user name>/Minecraft/m1-multimc-hack/mcwrap.py```

Replace the `<your user name>` with the username you got earlier. So for me it would be:\
```/Users/thatsniceguy/Minecraft/m1-multimc-hack/mcwrap.py```

Again make sure to replace the user name with your own or it wont work.\
<br>
<br>
<img width="766" alt="image" src="https://user-images.githubusercontent.com/10524728/141719260-dfd07960-56e8-4132-825d-8dd3d222e1d1.png">

This is how it should roughly look. Close the settings and make a new MultiMC instance like normal. Just make sure to use a recent version 1.16 or later. 1.17.1 is ideal.

Now launch the instance like normal (not offline). Let it log in and download the game assets.

Once it finishes it should launch minecraft like normal.

## Done
<img width="1062" alt="image" src="https://user-images.githubusercontent.com/10524728/141720108-4ce6c3b0-059e-4989-98c0-5637ae8b12a5.png">
Finished.

From here you can install Fabric from MultiMC by clicking Edit Instance, going to the Version tab and clicking 'Install Fabric'. Install 0.11.7 as thats the one that works. Then click 'Download All' and Fabric should now be installed.

From here, just edit like you normally would in MultiMC.
