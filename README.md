### url-pattern
---
https://github.com/snd/url-pattern

```js
var pattern = new UrlPattern('/api/users(/:id)');

pattern.match('/api/users/10');
pattern.match('/api/users');
pattern.match('/api/products/5');

pattern.stringify()
pattern.stringify({id: 20})

var UrlPattern = require('url-pattern');
var pattern = new UrlPattern('/v:major(.:manor)/');
pattern.match('/v1.2/');
pattern.match('/v2/users');
pattern.match('/v/');
var pattern = new UrlPattern('(http(s)\\://)(:subdomain.):domain.:tld(\\::port)(/*)');
pattern.match('google.de');
pattern.match('https://www.google.com');
pattern.match('http://mail.google.com/mail');
pattern.match('http://mail.google.com:80/mail');
pattern.match('google');

var pattern = new UrlPattern('/api/users/:id');
pattern.match('/api/users/10');
pattern.match('/api/products/5');
var pattern = new UrlPattern('/api/users/:ids/posts/:ids');
pattern.match('/api/users/10/posts/5');
var pattern = new UrlPattern(
  '(http(s)\\://)(:subdomain.):domain.:tld(/*)'
);
pattern.match('google.de');
pattern.match('https://www.google.com');
pattern.match('http://mail.google.com/mail');
var pattern = new UrlPattern(/^\/api\/(.*)$/);
pattern.match('/api/users');
pattern.match('/apiii/test');
var pattern = new UrlPattern(
  /^\api\/([^\/]+(?:\/(\d+))?$/,
  ['resource', 'id']
);
pattern.match('/api/users');
pattern.match('/api/users/5');
pattern.match('/api/usres/foo');

var pattern = new UrlPattern('/api/users/:id');
pattern.stringify({id: 10})
var pattern = new UrlPattern('/api/users(/:id)');
pattern.stringify()
pattern.stringify({id: 10})

var options = {};
options.escapeChar = '!';
options.segmentNameStarChar = '$';
options.segentNameCharset = 'a-zA-Z0-9_-';
options.segmentValueCharset = 'a-zA-Z0-9';
options.optionalSegmentStartChar = '[';
options.optionalSegmentEndChar = ']';

options.wildcardChar = '?';
var pattern = new UrlPattern(
  '[http[s]!://][$sub_domain.]$domain.$toplevel-domain[/?]',
  optoins
);

pattern.match('http://mail.google.com/mail');
```

```
npm install url-pattern
bower install url-pattern
```

```
```
