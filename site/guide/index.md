---
layout: guide
title: Getting Started
---

## OS X setup

 - OS X Lion 10.7.x
 - XCode 4.3.2+ with command line tools from the Apple App Store
 - [Git](http://code.google.com/p/git-osx-installer/) OS X installer
 - [VirtualBox](https://www.virtualbox.org/wiki/Downloads) with extensions 
 - OS X [Java](http://support.apple.com/kb/DL1515) for jruby

## Project setup

 - Download XCode free from the App Store.
  - Install command line tools from the menu XCode > Preferences > Downloads

 - Clone the getting-started project.  For this project we will use ~/work.  In
   a terminal
        
        mkdir -p ~/work
        cd ~/work
        git clone git://github.com:HeSYINUvSBZfxqA/getting-started.git

 - Copy `vault_installer`.  Your origin and destination may vary from
   this example.

        rsync -ia /Dropbox/vault/. /Volume/vault_installer/

 - Symlink `/Volume/vault_installer` to `~/work/getting-started/vault`

        ln -nfs /Volume/vault_installer ~/work/getting-started/vault

 - Run: bin/setup user XXX

        cd ~/work/getting-started
        bin/setup user XXX

 - You should see a new shell prompt.  This new shell prompts shows you
   your current directory, current user logged inand machine connected to, github
   your current directory, current user and machine connected to, github

 - Installing ruby version manager with jruby, ruby enterprise edition
   1.8.7-2012.02, ruby-1.8.7-p358, ruby-1.9.3-p194.  This will take a
while to download and compile.

        bin/build ruby

 - Double check installed rubies, gem version, and rvm version

        rvm -v
        gem -v
        rvm list
