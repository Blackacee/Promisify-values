# Promisify-values

let resolved = Promise.resolve(2);
resolved.then(value => {
 // immediately invoked
 // value === 2
});
If value is already a promise, Promise.resolve simply recasts it.
let one = new Promise(resolve => setTimeout(() => resolve(2), 1000));
let two = Promise.resolve(one);
two.then(value => {
 // 1 second has passed
 // value === 2
});
