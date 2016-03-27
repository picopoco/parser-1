##  jsonparser
Console utility that parses data from stdin and outputs them to the stdout

###  Usage:
```
$ tail -f /var/log/service.log | jsonparser
$ tail -f /var/log/service.log | jsonparser --format template.j2
$ tail -f /var/log/service.log | jsonparser --filter @fields.level=ERROR
```

###  Options:
--format    Tels parser to use given file as output template
--filter    Filters input lines by given fields value

###  Default output:
```
[@timestamp] @fields.level @message
```

###  Example:
```
$ tail -f /var/log/service.log | jsonparser
[2015-12-15T05:45:39+00:00] INFO Request processed
```
