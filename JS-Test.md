## Senior JS developer competency test

#### Task 1. Floats.

- [ ] Please explain why this code `console.log(0.1 + 0.2 == 0.3);` outputs `false` in console? 
- [ ] Please suggest fix to make this expression working as expected.

#### Task 2. Sum function.

- [ ] Write a `sum` function which will work properly when invoked using either syntax below: 

```javascript
console.log(sum(2,3)); // Outputs 5 
console.log(sum(2)(3)); // Outputs 5
``` 

- [ ] Make the function working for any number of arguments.

#### Task 3. Loops.

Consider you have code snippet like this: 

```javascript
for (var i = 0; i < 5; i++) {
  var btn = document.createElement('button');
  btn.appendChild(document.createTextNode('Button ' + i));
  btn.addEventListener('click', function(){ console.log(i); });
  document.body.appendChild(btn);
}
```

- [ ] What will be the output when user clicks on `Button 1` and why? 
- [ ] Please, suggest a fix to get the expected behavior.

#### Task 4. Cache buster function.

Write a JS function `cachebuster`.
- [ ] The function should return new unique value (string or integer) every 5 minutes. See example below.
- [ ] Make this function as short as it is possible.


```javascript
function cachebuster() {
 // your code goes here
}

console.log(cachebuster()); // Called immediately, outputs string or integer, e.g. "abcd" or 1234
console.log(cachebuster()); // Called after 1 minutes, outputs the same string: "abcd" or 1234
console.log(cachebuster()); // Called after 2 minutes, still outputs: "abcd" or 1234

// ...

console.log(cachebuster()); // Called after 5 minutes, outputs new unique value: e.g. "abce" or 1235
console.log(cachebuster()); // Called after 6 minutes, outputs previous value: "abce" or 1235

// ...

console.log(cachebuster()); // Called after 10 minutes, outputs another one new unique value, like "abcf" or 1236

```


## Instructions

- Please clone this repo in a new `Bitbucket` (or `GitHub`) private repo.
- Edit `README.md` file to provide answers on tasks `Tasks 1-4`. 
- Implement Angular JS app described in `Task 5` and push changes in your repo.
 

We suppose this test require from 2 to 3 hours. Thanks in advance for your time spent on this test! 
