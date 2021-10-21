### Задача 1
Коллега отправил вам файл, но вы нигде не можете найти константу VECTOR_NAME. Нужно восстановить ее, опираясь на этот блок кода.

```ecmascript 6
const getVector = ({x, y}) => {
    if (x > y) {
        if (Math.abs(x / y) < THRESHOLD) return;
        return x > 0 ? 3 : 1;
    } else {
        if (Math.abs(y / x) < THRESHOLD) return;
        return y > 0 ? 2 : 0;
    }
};

let v = getVector({x: _x, y: _y});
if (v && VECTOR_NAME.indexOf(v) !== -1) {
    ev.emit('event.' + VECTOR_NAME[v]);
}

ev.on('event.up', () => {
    console.log('Восхитительно, что-то движется вверх!');
});
```

Ответ:
