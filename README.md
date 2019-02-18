# Backgound

These are bash- and python- scripts that I have written over the years, for some prefer python and other bash. So i decided to re-work these scripts, standardized them and create them both in bash and python. These are meant to be running on a Linux system.

# Alerting
The scripts has 3 methods to alerting:
1. **Email** : it assumed the system if configured to use postfix (sendmail) to send email and is in working condition.
2. **Slack** : in the bash scripts it will call a python script that will need to be configured, while in the python version is built-in.
3. **Pagerduty** : same as the Slack alerting, the bash scripts it will call a python script that will need to be configured, and its built-in in the python version

Any of the Alerting can be disabled.
In the bash scripts set the following variables to **0**
1. _alert_email
2. _alert_slack
3. _alert_pd

In the python scripts set these variable to **0**
1. alert_email
2. alert_slack
3. alert_pd

# Configuration
## Bash scripts
These will need to be edited and adjusted, the start of the items to be configured is indicated with the **# start Configuration** up to the **# end Configuration**

## Python scripts
These requires a configuration file, the default location of the configuration file is **/etc/bao/<script-name.cfg>** or use the **-C** flag to override the default configuration file.

# Returning values
The script will return a **0** if the check passed and **2** if it failed. And the text displayed will always starts with either **OK** or **CRITICAL**, I understand that there could be other possibilities, such as the script fails to reach the check part, but I decided to handles this as and **CRITICAL** error as well and more information will be logged.

# Logging
Each script will write to a log file which is **/var/log/<script-name>.log**, it will rely on **logrotate** to rotate it log file. The name and location of the log file can be adjusted on your need, it part of the configurable option in bash and part of the configuration for the python scripts.


## Feedback
Feedback, bug report and requests for new scripts welcome...

**enjoy**
my10c
