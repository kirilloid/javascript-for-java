## types

### type system

Java has static strong type system.
JavaScript has dynamic weak type system.

In order to give you quick overview illustrate differences, I'll go with very simple example of what happens if we try to `+` a string and a number. In both languages this operator means numeric addition or string concatenation depending on context. The difference is how context is defined.
I'd also add Ruby to comparison, because it has dynamic, but strong typing.

```Java
int a = 1;
String s = "2";
return a + s;
```

- In Java it's just a compilation error;
- In Ruby it's a run-time error;
- In JavaScript it's just `"12"`—string type takes precedence

Actually, it's not that black and white with the strength of a type system. Ability to assign e.g. `long` to `int` w/o explicit conversion could be considered as a weakness in a type system.

If you'd like to learn more about static/dynamic, here's a [hillarious video about type systems' qualities](https://www.destroyallsoftware.com/talks/useing-youre-types-good) which demonstrate difference in type systems on Java and Ruby. SPOILER ALERT: It's very sarcastic so your feelings might be hurt if you think noone should attack your favorite Java.

But the summary is that type system in JavaScript is dynamic and significantly weaker.

### types and values

Basically JavaScript similarly has primitive and object/reference types. All primitive types have corresponding wrapper types and auto-boxing, like `int` - `Integer`, `long` - `Long`.

#### Primitives

There are three<a href="#note_1"><sup>1</sup></a> primitives in JavaScript:
- `boolean` that's the simplest one, the same as in Java. But since our type system is a dynamic one, there are no non-shortcut booolean operators. `&` is always bitwise AND, `&&` is always boolean AND.
- `string` in JavaScript is a primitive (with corresponding Object-wrapper), which can be compared with regular equality `==` operator. But in all other aspects JavaScript strings are immutable and UTF-16 based as in Java (and many other languages, actually).
- `number` there's only one numeric type in JavaScript and it roughly corresponds to double, but there are two nuances.
- * some operations trigger conversion ToSingedInt32 or ToUnsignedInt32 internally. For example, bitwise operators. There are no 32 bit integers, but if you don't use division, integers up to 52 bits could be safely represented, which is reflected in `Number.MAX_SAFE_INTEGER` static constant equaling `Math.pow(2, 53) - 1`.
- * there are typed arrays, which are so low-level, that they are even closer to C rather than Java. You can read more about [typed arrays on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Typed_arrays), but their uses are rare in real-life applications.

Corresponding Object wrapper types like `Boolean` exist, but they are almost not used. I even think they were added purely for consistency/interoperability with Java.

Primitives are passed by value as in any language. There are differences in closures, but that's not the most basic thing and we'll talk about them [later](../advanced/closures.md).

#### Referential types

Similarly to Java there's a basic `Object` "class", other inherits from it.
It has basic methods like `toString` defined on them and inherited by any other object.


<span id="note_1">1 — there are also Symbols, but we'd skip them for now</span>