pyglet-directions
=================

Just some directons on how to get pyglet setup on osx. Windows / Linux users come see me


## tl;dr

Just follow these steps (skip ones if you already have done it). More directions are below

1. Install XCode through the Mac App store
2. Install the command line tools 
3. Install homebrew (http://brew.sh)
4. Install extras (hg, curl) through homebrew
5. Install pyglet through hg
6. Download avbin
7. Install avbin
8. Test all the things!

## moar

### 1. Installing XCode
Open the mac app store, search for xcode, install

Q. Why do I have to install XCode?
A. Because OSX is a silly place and doesn't ship a compiler without forcing the developer download the whole XCode env...

### 2. Installing the command line tools
Open XCode(heads up, the initial load of XCode is SLOOOOOOOW) and accept the Terms of Use. Once this is done, open the preferences (cmd + ,) and go to downloads. From their select command line tools and install them.

Q. Why do I have to install the command line tools?
A. Because while XCode gets you a compiler, it doesn't include some of the helpful things for the command line.

### 3. installing homebrew
Now that you have installed x

### 4. Installing hg

````bash
brew install hg curl
````

### 5. installing pyglet through hg

````bash
hg clone https://pyglet.googlecode.com/hg/ && cd hg && sudo python setup.py install
````

In the cannonical documentation fashion, go get yourself a coffee as this step will take a while. Also you can download #6
### 6. Download avbin

````bash
curl https://github.com/downloads/AVbin/AVbin/avbin-darwin-x86-64-v8.1.tar.bz2
````

Now unpackage the file and cd into the directory.

````bash
tar -xvjf avbin-darwin-x86-64-v8.1.tar.bz2  && cd avbin-darwin-x86-64-v8.1 
````

### 7. Install avbin
````bash
sudo ./install.sh
````

### 8. Test all the things

Open the python shell and runn the following commands. Your output should look similarish.

````python
>>> import pyglet
>>> print(pyglet.version)
1.2alpha1
>>> print(pyglet.media.have_avbin)
2013-06-05 18:01:35.942 Python[9829:1307] ApplePersistenceIgnoreState: Existing state will not be touched. New state will be written to /var/folders/5q/2x6kltrj12s4wgb18hnbkrtc0000gn/T/org.python.python.savedState
True
>>> print(pyglet.media.avbin.get_version())
8
````
