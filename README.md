pyglet-directions
=================

Just some directons on how to get pyglet setup on osx. Windows / Linux users come see me


## tl;dr

Just follow these steps (skip ones if you already have done it). More directions are below

1. Install XCode through the Mac App store
2. Install the command line tools 
3. Install homebrew (http://brew.sh)
4. Install mercurial (hg) through homebrew
5. Install pyglet through hg
6. Download avbin
7. Install avbin
8. Test all the things!

## moar

### 1. Installing XCode


### 2. Installing the command line tools

### 3. installing homebrew

### 4. Installing hg

````bash
brew install hg
````

### 5. installing pyglet through hg

````bash
hg clone https://pyglet.googlecode.com/hg/ && cd hg && sudo python setup.py install
````

In the cannonical documentation fashion, go get yourself a coffee as this step will take a while. Also you can download #6
### 6. Download avbin

https://github.com/downloads/AVbin/AVbin/avbin-darwin-x86-64-v8.1.tar.bz2

### 7. Install avbin

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
