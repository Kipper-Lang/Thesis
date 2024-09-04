```js
isCompatibleWith(obj) {
    for (const field of this.fields) {
        if (!(field.name in obj)) {
            return false;
        }
    }
    for (const method of this.methods) {
        if (typeof obj[method.name] !== 'function') {
            return false;
        }
    }
    return true;
}
```