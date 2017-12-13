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
# python .\test.py .\test.txt
from sys import argv
script, filename = argv

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
# python .\test.py .\test.txt .\test_write.txt
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

<b>Functions</b>
```
def new_fucntion(arg1, arg2):
    print "hello man, one arg is %s and the second one is %s" % (arg1, arg2)

new_fucntion("toula", "yioula")

def print_two(*args):
    arg1, arg2 = args
    print "arg1: %r, arg2: %r" % (arg1, arg2)

print_two("yo 1", "yo 2")
```

<b>Read/Write & Functions</b>
```
from sys import argv

script, input_file = argv

def print_all(f):
    print f.read()

def rewind(f):
    f.seek(0)

def print_a_line(line_count, f):
    print line_count, f.readline()

current_file = open(input_file)

print_all(current_file)

rewind(current_file)

current_line = 1
print_a_line(current_line, current_file)
```

<b>IF loop</b>
```
car = 1
if car < 1: 
    print "ok 1"
elif car > 1:
    print "ok 2"
else:
    print "ok 3"
```

<b>For Loop</b>
```
numbers = [1, 2, 3]

for number in numbers:
    print "the number is %s" % number
```
