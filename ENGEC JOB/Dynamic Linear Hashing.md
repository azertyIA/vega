There's a midterm in two weeks... for Michael. Cheat sheet, yes. Indexing allows disk access to be more efficent. We accept the penalty of storing extra data because access time is prioritized. Indices are dictionaries and each pair is an item.

### SPEED
B trees have the parent nodes inside the final leaf nodes. Hashing is another way to quickly get data. Because pages are large, each page serves as a bucket that stores multiple items.

### Linear Hashing
Does not use modulus but uses some last bits of the number (so pretty much just modulus). When the items in one bucket hits 2n. You only have to rehash so many of the shits. When you get too big, you add a bucket or split an existing one. n goes up until it hits 2 to the i.