## Quickly add assertion methods
require 'test/unit/assertions'
include Test::Unit::Assertions

## Debugging
Get NewRelic debugging script from [https://github.com/newrelic/rpm/blob/master/bin/nrdebug](here) then run:
ruby nrdebug <pid>

## Parameters assignments
3 types:
* Required (R)
* Optional (O)
* Array (A)

def m(a, b=2, *c, d); end

m(1, 3) => a = 1, b = 2, c = [], d = 3
m(1, 3, 5) => a = 1, b = 3, c = [], d = 5
m(1, 3, 4, 5) => a = 1, b = 3, c = [4], d = 5


## Ruby metaprogramming

### prepend hook
http://gshutler.com/2013/04/ruby-2-module-prepend/

## StringIO

io = StringIO.new
io.write('abc')
io.rewind
io.read # returns 'abc'
