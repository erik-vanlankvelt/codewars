# codewars
Codewars problems and solutions

### Growth of a Population
[Problem](https://www.codewars.com/kata/563b662a59afc2b5120000c6)

Solution
```
function nbYear(p0, percent, aug, p) {
  let populationOverTime = p0;
  let years = 0;
  // Convert percent
  const convPercent = percent / 100;
  
  while (populationOverTime < p) {
    populationOverTime += Math.floor(populationOverTime * convPercent) + aug;
    years += 1;
  }
  
  return years;
}
```


### Multiples of 3 or 5
[Problem](https://www.codewars.com/kata/514b92a657cdc65150000006)

Solution
```
function solution(number) {
  // Check if the supplied value is a number
  if (isNaN(number)) {
    console.error(`${number} is not a number`);
  }
  
  // Return 0 if number is negative
  if (number < 0) {
    return 0;
  }
  
  let sumOfMultiples = 0;
  // Sum of all multiples below the number passed in
  for (let i = 0; i < number; i++) {
    // Count once if number is a multiple of both 3 and 5
    if (i % 3 === 0 || i % 5 === 0) {
      sumOfMultiples += i;
    }
  }
  
  return sumOfMultiples;
}
```

### Beginner Series #3 Sum of Numbers
[Problem](https://www.codewars.com/kata/55f2b110f61eb01779000053)

Solution
```
function getSum(a,b) {
  // Check if supplied values are numbers
  if (isNaN(a) || isNaN(b)) {
    console.error('Only numbers can be provided.')
  }
  
  // We only want to deal with whole numbers
  a = Math.round(a);
  b = Math.round(b);
  
  // If the two numbers are equal return a
  if (a === b) {
    return a;
  }
  
  const min = Math.min(a, b);
  const max = Math.max(a, b);

  return ((max - min) + 1) * (min + max) / 2;
}
```
