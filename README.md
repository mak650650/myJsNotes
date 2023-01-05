## Type conversion:-

```
There are two ways of type conversion:
 
>1. Explicit Type casting/conversion ---> "manual"
>2. Implicit Type casting/conversion ---> "Coereion"
```

as, 

```js
console.log("1" + 1)
```
output: "11"
 
and

```js
console.log("1" - 1)
```
output: 0

After a glance ,it seems bit  *confusing*, but after reading and doing some reasearch in offical documentation provided by <a href="https://262.ecma-international.org/10.0/#sec-abstract-operations">Ecmascript</a>, I founded that it is rather very easy concept which is just hidden by javascript.

Now for understanding coercion we must first understand ABSOLUTE OPERATIONS.

### Absolute operation:

![doc image](https://github.com/mak650650/myJsNotes/blob/2a2f5a076cb93b5ea8ba95ba126a3dec584a0784/ab.png)

*as the  above documentation describe, that these type of operations is-

- Not a part of javascript language 
- It is just used to explain the hidden part of javascript's  implicit type conversion.

#ToNumber:

<a href="https://262.ecma-international.org/10.0/#sec-tonumber">doc</a>
```js
console.log(1 - undefined) // as undefined -- NaN
```
output: NaN

```js
console.log(1 - null) // as null -- +0
```
output: 0

```js
console.log(1 - "61") // output-->60 as string is converted from "61" --> 61
console.log(1 - "1xxxdj79") // output -->  1 - NaN --> NaN
console.log(1- "0xa") // output --> 1 - 10 --> -9 as "0xa" is 
					//hexaDecimal(16) and it get converted to Decimal(10).
```
output: 61 , NaN ,-9

```js
console.log(1 - true) // output --> 1 - 1(true = +1) --> 0
console.log(1 - false) // output --> 1 - 0 (false = +0) --> 1
```
output: true --> 0 and false --> 1
