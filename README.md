[![Build Status](https://travis-ci.org/visforest/tail.svg)](https://travis-ci.org/visforest/tail)
[![Build status](https://ci.appveyor.com/api/projects/status/vrl3paf9md0a7bgk/branch/master?svg=true)](https://ci.appveyor.com/project/Nino-K/tail/branch/master)


NOTE: This repo is forked from [https://github.com/hpcloud/tail](https://github.com/hpcloud/tail) (main branch) which hasn't been maintained for long time. I abandoned vendor, and fixed its import problem. 

# Go package for tail-ing files

A Go package striving to emulate the features of the BSD `tail` program. 

```Go
t, err := tail.TailFile("/var/log/nginx.log", tail.Config{Follow: true})
for line := range t.Lines {
    fmt.Println(line.Text)
}
```

See [API documentation](http://godoc.org/github.com/visforest/tail).

## Log rotation

Tail comes with full support for truncation/move detection as it is
designed to work with log rotation tools.

## Installing

    go get github.com/visforest/tail/...

## Windows support

This package [needs assistance](https://github.com/visforest/tail/labels/Windows) for full Windows support.
