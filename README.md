# LeetCode 299 - Bulls and Cows

## Problem Statement

You are given two strings, `secret` and `guess`.

A **bull** means a digit is correct and in the correct position.

A **cow** means a digit is correct but appears in the wrong position.

Return the hint in the format:

```text
xAyB
```

where `x` is the number of bulls and `y` is the number of cows.

## Example

### Input

```text
secret = "1807"
guess = "7810"
```

### Output

```text
"1A3B"
```

### Explanation

* `8` is a bull because it is in the correct position.
* `1`, `0`, and `7` are cows because they exist in `secret` but are in different positions.

## Approach

First count the digits that match at the same position.

For the remaining digits, count how many times each digit appears in both strings. The minimum count gives the number of cows.

## Algorithm

1. Initialize the bull count.
2. Compare corresponding digits.
3. If they match, increase `bulls`.
4. Otherwise, store their frequencies.
5. For each digit from `0` to `9`, add the minimum frequency to `cows`.
6. Return the result as `xAyB`.

## Time Complexity

**O(n)**

## Space Complexity

**O(1)**

Only 10 digit counts are stored.

## Author

T. Nandhini
