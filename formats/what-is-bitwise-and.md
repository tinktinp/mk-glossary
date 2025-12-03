# What is "bit-wise and"
The `&` operator, which I pronounce "and" is more formally called the "bit-wise AND operator".

If `lhs` is the "left hand side", and `rhs` is the "right hand side", and if you do:

```js
const result = lhs & rhs;
```

Then here's some pseudo-code (fake code) that shows how it works:

```js
function bitwise_and(lhs, rhs) {
    const numberOfBits = 32;

    let result = 0; // default to all zeros

    for (let i = 0; i < numberOfbits; i++) {
        if (lhs[i] === 1) {
            if (rhs[i] === 1) {
                result[i] = 1;
            }
        }
    }
    return result;
}
```

(You can't really index numbers like that to access their bits. That's the part that's fake above.)