# python
```
http://www.souravsengupta.com/cds2015/python/LPTHW.pdf
https://www.python.org/dev/peps/pep-0008/
```

```
from sys import argv
script, filename = argv

# script, first, second, third = argv

# print "first argv", script
# print "first argv", first
# print "first argv", second
# print "first argv", third
# and run `python test.py first 2nd 3rd

print "hello python"

car = 'VW'
bike = 'Yamaha'
print "my car is %s and my bike is %s" % (car, bike)

formatter = "%r %r %r %r"
print formatter % (1, 2, 3, 4)

print """
gefae fgefa
feafea
feafaf fafeaf
"""

print "\nHello"

print "how old are you?"
age = int(raw_input())
print "you are %s" % age

name = raw_input("my name is? ")
print "So, your name is %s" % name

```

<b>Read/Write File</b>
```
from sys import argv
script, filename = argv

# python .\test.py .\test.txt
print "name file %r" % filename

# assign object file
target = open(filename, 'w')
# print target.read()

# empty file
target.truncate()

# write 
line1 = raw_input("line 1: ")
target.write(line1)
target.write("\n")
line2 = raw_input("line 2: ")
target.write(line2)
```
<b>Read/Write from one file to another</b>
```
from sys import argv
from os.path import exists

script, from_file, to_file = argv

print "Copying from %s to %s" % (from_file, to_file)

in_file = open(from_file)
indata = in_file.read()

print "read %d" % len(indata)

out_file = open(to_file, 'w')
out_file.write(indata)

out_file.close()
in_file.close()
```
