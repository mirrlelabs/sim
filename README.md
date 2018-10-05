# sim
sim | simple text importer aka simsalabim

## Parameter Overview

``` 
cat /var/logs/apache2/project.log | sim 

  -h | --help                                 # shows this:
  -l | --lang python                          # set syntax language to python, (default: plaintext)
  -T | --theme night                          # set the web theme to night theme (default: icecoder)
  -L | --list                                 # list all themes and syntaxes
  -t | --time 10M|1D|2W|1Y|1m|4h|0            # set livetime month,day,week,year,minute,hour,0=endless (default: 7 days|7D)
  -P | --privacy [public|private]             # set privacy mode (default: private)
  -S | --subject "filtered logs"              # the title

Future Params: 
  -c | --config "/path/to/config.file"        # later: we can setup some standard settings as a default tbd, read from /etc/sim.conf or ~/.sim.cfg (yaml/ini/toml)...
  -o | --output [yaml|json|toml|...]          # later: output format
  -C | --crypt <strongpassword>               # later: sim encrypts the text with a password and generates a hash, wich you can use on website?
  -p | --proxy http[s]://proxyserver:port     # later: placeholder for proxy settings
  -A | --api http://foo/bar/API               # later: if someone use a own sim-web-server? tbd
  -m | --module [jira|opsgenie|git|telegram]  # for the future: maybe we have a number of modules to connect them to other platforms, It seems like a good idea (simple text importer from commandline)
  -e | --email "subject..." [name@domain.tld] # send mail to someone :-) 
```
