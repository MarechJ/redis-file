Credit goes to @daniellawrence
==============================

I just added a parameter not to delete the key, and 'w', 'a', 'r' modes.
There's still some improvements to be done to match the file interface.


redis-file
==========

This is a simple hack to allow the writing to redis as if it was just file object in python.

Usage
-----

```python
    # Import and open up a ne "file"
    from redisfile import RedisFile
    f = RedisFile("myrediskey")
    # Write some lines to the "file"
    f.write('hello')
    f.writelines('world')
    f.writelines('Your\nAwesome')
    # Read the whole file
    print f.read()
    # Reading a file from the end shows no data
    print f.read()
    # seek to the start of the file
    f.seek(0)
    # Read a single line
    print f.readline()
    # Read the rest
    print f.read()
    # "close" will delete all the data
    f.close()
```

Installation
------------

Installation is simple too::

    $ python setup.py install
