# gpgenv


## What ??
Gpgenv is similar to envdir and dotenv, but it lets you use gpg-encrypted files. This is useful if you want to store sensitive credentials on your machine, but you want to keep them encrypted.

It also removes comments in env file.

This readme assumes that you know how gpg works.

## Install

Clone this somewhere on your computer and add the path in your shell profile

## usage

    $> gpgenv <YOURENVFILE.gpg>  <CMD>


You can chain gpgenv to use multiple encrypted env files

    $> gpgenv db.env.gpg  gpgenv service.env.gpg ./deploy-my-service-plz.sh

# create an Env file

Your env file should be at the format

    KEY=value


You can encrypt your file like any other file with gnuPg cli

    $> gpg -e -r <identity> <your_clear_env_file>


# todo  

  - allow the user to use a directory
  - add profiles management
