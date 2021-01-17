# big-sur-install
This playbook is for the installation of Mac Applications for the Apple Store on macOS 11.x

# Important Note
This uses the mas client (which needs to be installed using homebrew). Unfortunately the Ansible MAS client module does not have a way to 'purchase' apps (rather than install) that have never been installed on your Mac before. Therefore not terribly useful on clean Mac installs.

For now I have added a block / rescue section to catch errors and then issue 'mas purchase [id]' using the command module to work around this but it is kind of ugly...
