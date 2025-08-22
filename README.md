```markdown
# Golf Score Translator

## Overview
The Golf Score Translator is a simple JavaScript function that converts the number of strokes taken on a hole into a corresponding golf nickname based on the par value of the hole. This helps golfers quickly understand their performance relative to the expected par.

## Objective
Create a function named `golfScore` that takes two numeric arguments:
- `par`: The expected number of strokes for the hole.
- `strokes`: The actual number of strokes taken.

The function should return a string nickname describing the score based on the following rules:
- "Hole-in-one!" if strokes is 1.
- "Eagle" if strokes is less than or equal to par minus 2.
- "Birdie" if strokes is exactly par minus 1.
- "Par" if strokes equals par.
- "Bogey" if strokes equals par plus 1.
- "Double Bogey" if strokes equals par plus 2.
- "Go Home!" if strokes is greater than or equal to par plus 4.

## Usage
Call the function with the par value and strokes:
```javascript
console.log(golfScore(4, 1)); // Output: Hole-in-one!
console.log(golfScore(4, 2)); // Output: Eagle
console.log(golfScore(4, 7)); // Output: Go Home!
``

## Implementation

```javascript
/**
 * Returns the golf score nickname based on par and strokes.
 *
 * @param {number} par - The par value of the hole.
 * @param {number} strokes - The number of strokes taken.
 * @returns {string} - The nickname describing the score.
 */
function golfScore(par, strokes) {
  if (strokes === 1) {
    return "Hole-in-one!";
  } else if (strokes <= par - 2) {
    return "Eagle";
  } else if (strokes === par - 1) {
    return "Birdie";
  } else if (strokes === par) {
    return "Par";
  } else if (strokes === par + 1) {
    return "Bogey";
  } else if (strokes === par + 2) {
    return "Double Bogey";
  } else if (strokes >= par + 3) {
    return "Go Home!";
  }
}

``

## Testing
You can test the function with various inputs:
```javascript
console.log(golfScore(4, 1)); // "Hole-in-one!"
console.log(golfScore(4, 2)); // "Eagle"
console.log(golfScore(4, 3)); // "Birdie"
console.log(golfScore(4, 4)); // "Par"
console.log(golfScore(4, 5)); // "Bogey"
console.log(golfScore(4, 6)); // "Double Bogey"
console.log(golfScore(4, 7)); // "Go Home!"
console.log(golfScore(5, 9)); // "Go Home!"
``

## License
This project is for educational purposes.
```

Feel free to customize the README with your project-specific information or additional instructions!
