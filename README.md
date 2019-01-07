# mangarock-ded


## android 3.75 (2019-01-04)

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
