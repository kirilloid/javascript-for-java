## Containers

Basically there are two types of containers/collections: `Array` and `Object`.

### Array

JavaScript array is an `ArrayList<Object>`. There might be any combination of values of different types. But JIT optimizators are able to generate more performant representation and code for monotyped arrays, e.g. array of numbers.
Also storing apples with apples and oranges with oranges usually is logical for the people who are going to read this code. So values of different types are not mixed in one array very often in JavaScript.

### Object

Due to dynamic nature of JavaScript a property with any name could be added to an Object at run-time even w/o some reflection "magic". This is the basic language capability. So roughly every Object could be also viewed as a `Map<String, Object>` with all operations on properties executed in O(1) amortized time.

Being able to add any property to any object doesn't mean that every object instance is a special snowflake and there's no consistency. Similary to arrays, JIT optimizes operations for objects with the same structure. For examples, if one'd create points as objects with two properties: `x` and `y`, the code would be very efficient and accessing any of those two properties would be compiled into reading from a pointer + constant offset, just like a program has been implemented in C.
The point about understanding by others also holds here.

### Set/Map

In es2015 a new kind of containers were added to the standard and most modern (2018) browsers support them: Set, Map, WeakSet and WeakMap.
- Set is `Set<Object>`
- Map is `Map<Object, Object>`
Weak counterparts are the same except that references to keys are not counted when it's time for garbage collection.