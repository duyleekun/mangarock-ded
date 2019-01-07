# mangarock-ded

Mangarock got reversed enginerred

Tool used:

- CFR
- Xposed
- MITM
- Frida

## android 3.75 (2019-01-04)

They changed their hashing algorithm to XXhash (fast and secure hashing algorithm) and the secret in the hash was generated from a single function, I didn't even bother to read the code.

CloudFlare blocked my crawling server for the first time

- Endpoint `https://api.mangarockhd.com/query/android375/`

- Headers

```
{
  'QToken': token(url),
  'Device': 'zAMFdi5nFx',
}
```

- Token

```ruby
'3'+XXhash.xxh64("#{url}:37184c86f461744eacf1e0422ee42c8acd678e25c6d06f06b7d723721e331270",0).to_s(16)
```

## android 3.63 (2018-10-18)

This time they start to verify QToken

- Endpoint `https://api.mangarockhd.com/query/android312/`

- Headers

```
{
  'QToken': token(url),
  'Device': 'zAMFdi5nFx',
}
```

- Token

```ruby
md5(md5(md5(url)+"mr")+"nabvn")
```

## android 3.12 (2017-10-27)

- Endpoint `https://api.mangarockhd.com/query/android312/`

- Headers

```
{
  'QToken': token(url),
  'Device': 'zAMFdi5nFx',
}
```

- Token

```ruby
md5(md5(md5(url)+"mr")+"nabvn")
```

## ios 3.83 (2017-05-08)

They introduced ReactNative code inside their binary and leak the Token generator in the JS code. Their server didn't validate the `QToken` at that time.

- Endpoint `https://api.mangarockhd.com/query/ios383/`

- Headers

```
{
  'QToken': token(url),
  'Device': 'zAMFdi5nFx',
}
```

- Token

```ruby
md5(md5(md5(url)+"mr")+"nabvn")
```



## 0.4040 (2015-05-10)

- Endpoint `http://mr2.mangarockhd.com/queryv2/mrquery4040world.php`
- No signing required

## 0.4020 (2014-08-07)

- Endpoint `http://mr2.mangarockhd.com/queryv2/mrquery4020world.php`
- No signing required

## 0.4012 (2014-07-02)

- Endpoint `http://mr2.mangarockhd.com/queryv2/mrquery4012world.php`
- No signing required

# Want your app got DED?

Contact me and we can have a talk.
