# c11n

Yet another gem to store app configuration.

## Interface

Super simple interface to use.

```
> C11n[:key]
"value"

> C11n[:key2] = { :foo => :bar }
{ :foo => :bar }

> C11n.all
{ :key => "value", :key2 => { :foo => :bar }
```

## Features

* Different storage options

  * YAML
  * ActiveRecord
  * Key-Value

* Caching in memory

* Backend chaining
`C11n.backend = C11n::Backend::Cache.new(C11n::Backend::ActiveRecord.new(C11n::Backend::Simple.new()))`

