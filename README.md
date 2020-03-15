# gpgenv


This script allow to eval and run command with a GPG encrypted env file

This readme assumes that you know how gpg works.

## usage

    $> gpgenv <YOURENVFILE.gpg>  <CMD>


You can chain gpgenv to "concat" multiple encrypted env

    $> gpgenv db.env.gpg  gpgenv service.env.gpg ./deploy-my-service-plz.sh

# create an Env file

    $> gpg -e -r <identity> <your_clear_env_file>
