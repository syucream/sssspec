# sssspec

A simple Serverspec executer by using mruby, named as Single Shot ServerSpec :zap:

## Quickstart

1. Write your Serverspec file at mrblib/sssspec.rb.

```
def __main__(argv)
  describe file('mrblib') do
    it { should be_readable.by('yourgroup').by_user('you') }
  end
end
```

2. Build sssspec binary.

```
$ rake
```

3. Copy ./mruby/bin/sssspec to a test target host.

4. Run sssspec and get its result :)

```
$ ./sssspec
.
Total: 1
   OK: 1
   KO: 0
Crash: 0
 Time: 0.16 seconds<Paste>
```

## Acknowledgement

This project is inspired by [mitamae](https://github.com/itamae-kitchen/mitamae).

