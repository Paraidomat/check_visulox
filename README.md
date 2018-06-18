# `check_visulox`

A Nagios compliant check for Oracle Secure Global Desktop and Visulox 

## Installation

1. Just throw the file into the plugin directory of your monitoring solution.
2. Add the commands to `visudo`:
   ```
   ## Allow Icinga to run tarantella commands
   icinga  ALL=NOPASSWD: /opt/tarantella/bin/tarantella status
   icinga  ALL=NOPASSWD: /opt/visulox/bin/visulox status
   icinga  ALL=NOPASSWD: /opt/visulox/bin/viuslox license
   icinga  ALL=NOPASSWD: /opt/visulox/bin/visulox online -format csv
   icinga  ALL=NOPASSWD: /bin/netstat -np
   ```

