# Notes





## ToDos


- [ ]  convert all dates to utc e.g. use DateTime#utc - why? why not?
       - example: 2015-01-16 08:33:57 UTC <= rfc822 Fri, 16 Jan 2015 09:33:57 +0100
       - or 2017-05-17 15:02:12 UTC <= iso8601 2017-05-17T08:02:12-07:00
       - and so on

- [ ]  check intertwingly.atom feed - uses relative urls - how to make absolute ??
       - feed.url:       /blog/
       - feed.items[0].url:      /blog/2017/04/07/Badges-We-dont-need-no-stinkin-badges


- [x]  change feed.generator_uri to generator_url  (keep uri as alias)

- [ ]   turn gernerator into a struct (instead of three strings)   
        - use generator.name, generator.url, generator.version, etc.
        - add alias for generator.name == generator.title  e.g. name = title



## Limitations of Stdlib RSS reader

### RSS 2.0

Cannot read feed_url link using atom:link type="self" e.g.:

```
<atom:link href="https://www.nostarch.com/feeds/comingsoon.xml?startat=tcpip"
           rel="self"
           type="application/rss+xml" />

<atom:link href="https://pragprog.com/feed/global"
           rel="self"
           type="application/rss+xml"/>

```

see books/nostarch.rss2 and others as examples.