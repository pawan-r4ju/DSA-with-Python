# Data Structures in Python for DSA

This notebook contains all the commonly used data structures in Python for **Data Structures and Algorithms (DSA)**, along with their methods. Each data structure is explained with methods that are commonly used in competitive programming and problem-solving.

## 1. Lists (Arrays in Python)

- Lists are dynamic and can store mixed data types.

- Used for sorting, searching, dynamic programming, etc.

### Methods:

- `append(x)` → Add an element at the end.

- `insert(i, x)` → Insert element `x` at index `i`.

- `remove(x)` → Remove the first occurrence of element `x`.

- `pop(i)` → Remove and return element at index `i`.

- `clear()` → Remove all elements.

- `extend(iterable)` → Append all items from an iterable (list, tuple, etc.).

- `index(x)` → Return the index of the first occurrence of `x`.

- `count(x)` → Count occurrences of `x`.

- `sort()` → Sort the list in ascending order.

- `reverse()` → Reverse the list in place.

- `copy()` → Return a shallow copy of the list.

- `len()` → Returns the number of elements.

- `del` → Used for deleting an element or slice (`del arr[2]`).

```python

arr = [1, 2, 3, 4, 5]

arr.append(6)  # Adds 6 to the end

arr.pop()  # Removes and returns 6

arr.sort()  # Sorts the list in ascending order

```

## 2. Strings

- Strings are immutable sequences of characters.

- Used for pattern matching, substring problems, and hashing.

### Methods:

- `upper()` → Convert string to uppercase.

- `lower()` → Convert string to lowercase.

- `title()` → Convert to title case.

- `strip()` → Remove leading/trailing whitespace.

- `split(sep)` → Split the string by separator `sep`.

- `join(iterable)` → Join the iterable using the string as a separator.

- `replace(old, new)` → Replace occurrences of `old` with `new`.

- `find(sub)` → Return the lowest index of substring `sub`.

- `count(sub)` → Count the number of occurrences of `sub`.

- `startswith(prefix)` → Check if the string starts with `prefix`.

- `endswith(suffix)` → Check if the string ends with `suffix`.

- `splitlines()` → Split string into a list by line breaks.

- `len()` → Get the length of the string.

```python

s = 'hello world'

print(s.upper())  # Output: 'HELLO WORLD'

print(s.find('world'))  # Output: 6

```

## 3. Hashing (Dictionaries and Sets)

- **Dictionaries (`dict`)** are key-value stores.

- **Sets (`set`)** are unordered collections of unique elements.

### Dictionaries Methods (`dict`):

- `dict[key]` → Access value by key.

- `dict.get(key)` → Return value for `key`, or `None` if not found.

- `dict.update(d)` → Update dictionary with items from `d`.

- `dict.keys()` → Return a view object of all keys.

- `dict.values()` → Return a view object of all values.

- `dict.items()` → Return a view object of key-value pairs.

- `dict.pop(key)` → Remove and return value for `key`.

- `dict.popitem()` → Remove and return an arbitrary (key, value) pair.

- `dict.clear()` → Remove all items from the dictionary.

### Sets Methods (`set`):

- `set.add(x)` → Add element `x` to the set.

- `set.remove(x)` → Remove element `x` from the set.

- `set.discard(x)` → Remove `x` from the set if it exists (doesn't raise error).

- `set.pop()` → Remove and return an arbitrary element.

- `set.clear()` → Remove all elements from the set.

- `set.update(iterable)` → Add all items from iterable to the set.

- `set.intersection(other_set)` → Return the intersection of two sets.

- `set.union(other_set)` → Return the union of two sets.

- `set.difference(other_set)` → Return elements present in the set but not in the other set.

- `set.symmetric_difference(other_set)` → Return elements that are in either set, but not both.

```python

d = {'a': 1, 'b': 2}

d.get('a')  # Output: 1

d.keys()  # Output: dict_keys(['a', 'b'])

s = {1, 2, 3}

s.add(4)  # Adds 4 to the set

```

## 4. Stacks (Using Lists or `deque`)

- **LIFO (Last In, First Out)**

- Used in DFS, backtracking, and expression evaluation.

### Using List (LIFO):

- `append(x)` → Push `x` onto the stack.

- `pop()` → Pop the last element from the stack.

### Using `collections.deque` (Optimized):

- `append(x)` → Add element `x` to the right end.

- `appendleft(x)` → Add element `x` to the left end.

- `pop()` → Remove and return element from the right end.

- `popleft()` → Remove and return element from the left end.

- `clear()` → Remove all elements.

- `extend(iterable)` → Add all items from iterable to the right.

- `extendleft(iterable)` → Add all items from iterable to the left.

```python

from collections import deque

stack = deque()

stack.append(1)

stack.pop()  # Removes and returns 1

```

## 5. Queues (`deque` or `queue.Queue`)

- **FIFO (First In, First Out)**

- Used in BFS, task scheduling.

### Using `collections.deque`:

- `append(x)` → Add element to the right end.

- `appendleft(x)` → Add element to the left end.

- `pop()` → Remove and return element from the right end.

- `popleft()` → Remove and return element from the left end.

### Using `queue.Queue` (Thread-Safe):

- `put(x)` → Add `x` to the queue.

- `get()` → Remove and return an element from the queue.

- `queue.empty()` → Check if the queue is empty.

- `queue.full()` → Check if the queue is full.

```python

from collections import deque

queue = deque()

queue.append(1)

queue.popleft()  # Removes and returns 1

```