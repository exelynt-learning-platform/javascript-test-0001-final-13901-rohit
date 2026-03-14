// Pattern size constant
const PATTERN_SIZE = 5;

// Function to generate a row of the pattern
function generateRow(i, n) {
    let row = "";

    // spaces
    for (let j = 1; j <= n - i; j++) {
        row += " ";
    }

    // stars
    for (let j = 1; j <= (2 * i - 1); j++) {
        if (j === 1 || j === (2 * i - 1)) {
            row += "*";
        } else {
            row += " ";
        }
    }

    console.log(row);
}

// Upper part of diamond
for (let i = 1; i <= PATTERN_SIZE; i++) {
    generateRow(i, PATTERN_SIZE);
}

// Lower part of diamond
for (let i = PATTERN_SIZE - 1; i >= 1; i--) {
    generateRow(i, PATTERN_SIZE);
}
