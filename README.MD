Install Ansible on Mac OS

Prerequisites -->  Xcode Command Line Tools

sudo xcode-select --install
sudo xcode-select -p
/Applications/Xcode.app/Contents/Developer
Agree to xcode license agreement: sudo xcodebuild -license


mymac$ python --version
Python 2.7.10

Install pip --> sudo easy_install pip

mymac$ pip --version
pip 9.0.1 from /Library/Python/2.7/site-packages/pip-9.0.1-py2.7.egg (python 2.7)


Install ansible --> sudo -H pip install ansible

mymac$ ansible --version
ansible 2.3.2.0
  config file =
  configured module search path = Default w/o overrides
  python version = 2.7.10 (default, Feb  7 2017, 00:08:15) [GCC 4.2.1 Compatible Apple LLVM 8.0.0 (clang-800.0.34)]

Configure Ansible

By default, Ansible uses password-less SSH to communicate with remote systems. Authentication is done using server keys. Each host needs to have a server key and ansible master host needs to be in the authenticated server list on each target hosts.

Refer to 'key based authentication' and SSH configuration specifics, before using the ansible toolkit.
https://robferguson.org/blog/2014/04/10/installing-ghost-step-2/#keybasedauthentication
https://robferguson.org/blog/2014/04/10/installing-ghost-step-2/#createasshconfigfile

AppDynamics Ansible toolkit consists of basic roles to install and configure machine agent and java agent modules. Currently, machine agent is not configured as service. Java agent can be configured to report to a specific controller. And application specific configuration are specified as JVM startup arguments.


Roles:

configureHost - Setup and update the host with necessary software

install-machineagent - Installs the machine agent files

start-machineagent - Restarts the machine agent

install-javaagent - Installs the java agent files

configure-javaagent - Configures the java agent to report to a specified controller
