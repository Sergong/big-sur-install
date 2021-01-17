# big-sur-install
This playbook is for the installation of Mac Applications for the Apple Store on macOS 11.x

# Important Note
This uses the mas client (which needs to be installed using homebrew). Unfortunately the Ansible MAS client module does not have a way to 'purchase' apps (rather than install) that have never been installed on your Mac before. Therefore not terribly useful on clean Mac installs.

For now I have added a block / rescue section to catch errors and then issue 'mas purchase [id]' using the command module to work around this but it is kind of ugly...

Also important to note is that you should set your Apple ID media and purchase preferences to never ask in System Preferences / Apple ID for this playbook to work.
At the moment it will still show an App Store prompt for Apps that haven't been installed :(