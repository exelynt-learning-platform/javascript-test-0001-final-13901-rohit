const PATTERN_SIZE = 5;

function generateRow(i, n) {
    let row = "";

    for (let j = 1; j <= n - i; j++) {
        row += " ";
    }

    for (let j = 1; j <= (2 * i - 1); j++) {
        if (j === 1 || j === (2 * i - 1)) {
            row += "*";
        } else {
            row += " ";
        }
    }

    console.log(row);
}

for (let i = 1; i <= PATTERN_SIZE; i++) {
    generateRow(i, PATTERN_SIZE);
}

for (let i = PATTERN_SIZE - 1; i >= 1; i--) {
    generateRow(i, PATTERN_SIZE);
}
