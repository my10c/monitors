# Backgound

These are bash- and python- scripts that I have written over the years, for some prefer python and other bash. So i decided to re-work these scripts, standardized them and create them both in bash and python.

# Alerting
The scripts has 3 methods to alerting:
1. **Email** : it assumed the system if configured to use postfix (sendmail) to send email and is in working condition.
2. **Slack** : in the bash scripts it will call a python script that will need to be configured, while in the python version is built-in.
3. **Pagerduty** : same as the Slack alerting, the bash scripts it will call a python script that will need to be configured, and its built-in in the python version

# Configuration
## Bash scripts
These will need to be edited and adjusted, the start of the items to be configured is indicated with the **# start Configuration** up to the **# end Configuration**

## Python scripts
These requires a configuration file, the default location of the configuration file is **/etc/bao/<script-name.cfg>** or use the **-C** flag to override the default configuration file.


**enjoy**
my10c
