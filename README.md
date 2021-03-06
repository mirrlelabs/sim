# sim
sim | simple text importer aka simsalabim, https://sim.do

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
  -H | --history 10                           # shows the last 10 entries (default 10, max 200)
  -s | --search "foo bar"                     # search a "string" by subject and printout url, combine with -o
```

## Future Parameters 

``` 
  -c | --config "/path/to/config.file"        # later: we can setup some standard settings as a default tbd, read from /etc/sim.conf or ~/.sim.cfg (yaml/ini/toml)...
  -o | --output [yaml|json|toml|short|plain]  # later: output format
  -C | --crypt <strongpassword>               # later: sim encrypts the text with a password and generates a hash, wich you can use on website?
  -p | --proxy http[s]://proxyserver:port     # later: placeholder for proxy settings
  -A | --api http://foo/bar/API               # later: if someone use a own sim-web-server? tbd
  -m | --module [jira|opsgenie|git|telegram]  # for the future: maybe we have a number of modules to connect them to other platforms, It seems like a good idea (simple text importer from commandline)
  -e | --email "subject..." [name@domain.tld] # send mail to someone :-) 
```


## Example Output after import

```
Title: "text text text"
Url: https://url.yourdomain.com/577c4bba7d6b551b70e76d95accc158c
Raw: https://url.yourdomain.com/577c4bba7d6b551b70e76d95accc158c/raw
Theme: night
Lines: 4238
Language: python
````
