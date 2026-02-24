Storage is fundamental. Most storage is stored on a disk or SSD. The idea is that data can be stored somewhere persistently even after the power is removed from the system. It is similar to writing on paper that you get to keep. A hard disk usually involve magnetic domains that get read and written to.

The surfaces of the platters are divided into tracks and blocks (4-8k). The disk drive only takes simple commands (read block, write to block, read blocks). The drive itself doesn't know anything about files or structures.

The database creates a logical view of the data, while the disk is the physical, low-level layer. In order to store something like a database table on a disk drive we need a logical to physical map.

In the relational model, the scheme includes:
- attributes (columns)
- tuples (rows)
- relations (tables)

To be model neutral the following terms will be used:
- field for a value
- record for a group of fields
- collection for a group of records

A DBMS may use a filesystem, but it can also do its own thing. For example, pages may be used to access data bigger than an individual block.

### Mapping Records to Physical

Different records require different amounts of metadata regarding the data, like the types and the lengths of the fields, records or collections. Each character is a byte, each integer takes 4 (word), and offsets take 2 (half). 

In general use fixed-lengths for your records. You could allocate the maximum possible length. You waste a lot of space, but it's very easy to store and address. If its smaller than the max, then you usually use a delimiter. You also just need some offsets to find certain data.

But if you have to use XML, then you have to use variable-length records. More metadata is needed in order to determine the boundaries and the locations (not even talking about moving), but you get a lot more space. You usually use per-record metadata (read the metadata to jump to the next record, read the metadata to jump to the value).

Some of the options we have:
1. Use a delimiter to separate the data. (`a#bc#d#`)
2. Precede each field by its length. (`1a2bc1d`)
3. Precede each record by the fields' offsets. (`89bcabcd`)

To represent null values, you could:
1. use an "out-of-band" value for every data type
2. use a special offset