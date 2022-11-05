# puzzle

This is a prototype serverless api implemented in Rust which generates a Sudoku puzzle & it's solution.  The resulting data is used by clients to display the puzzle and help the user solve it.

This is all built on top of this crate:

[![sudoku][badge-sudoku]][sudoku]

## deployed

- [puzzle][puzzle-io] -- _API_
- [sudoku][sudoku-io] -- _prototype app_

## sample

```
{
  "metrics": {
    "counts": {
      "blanks": 55,
      "clues": 26
    },
    "nanos": {
      "generate": 207810,
      "solve": 4550
    }
  },
  "puzzle": ".9..3....5.1.6.7..4..5.2.1.3.9..45...5..23......7...9.......14....2....68.6.....3",
  "ref": "Mjk3ODMxNDY1NTgxNDY5NzMyNDYzNTcyODE5MzE5Njg0NTI3NzU0OTIzNjgxNjI4NzE1Mzk0OTcyMzU2MTQ4MTM1MjQ4OTc2ODQ2MTk3MjUz",
  "tag": "netlify"
}
```

| Property | Description |
| ---: | :--- |
| **metrics** | _insight into the puzzle counts & times_ |
| **puzzle** | _a string representing the puzzle board (dots are blank cells)_ |
| **ref** | _the base64 encoded solution to the puzzle_ |
| **tag** | _platform_ |

[sudoku]: https://crates.io/crates/sudoku
[badge-sudoku]: https://img.shields.io/badge/crates.io-sudoku-orange

[sudoku-io]: https://rust-sudoku-wc.netlify.app/
[puzzle-io]: https://rust-sudoku-wc.netlify.app/.netlify/functions/puzzle

