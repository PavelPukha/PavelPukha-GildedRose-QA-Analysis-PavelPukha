# Gilded Rose QA Testing Report

## Scope
Manual testing of the Kotlin version of the Gilded Rose inventory logic.  
Goal. Verify that the current implementation follows the business rules described in the assignment.

## Main rules
1. Every item has SellIn and Quality values.
2. Normal items lose 1 Quality per day, and 2 after the sell date.
3. Aged Brie increases Quality every day until it reaches 50.
4. Backstage Passes increase by +1, +2, +3 depending on days left, then drop to 0 after the concert.
5. Sulfuras never changes — its Quality always stays 80.
6. Conjured items lose Quality twice as fast as normal ones.
7. Quality is always between 0 and 50, except Sulfuras.
8. Unrecognized item names behave like normal items.

Note. Testing checks only the UpdateQuality behavior; the Item structure stays unchanged.

## Test design
Plan. Focus on 10 main test cases that cover all rules and boundary values (0, 50, and negative SellIn).  
Each test simulates one day update for a single item.  
Extra cases for Conjured and Backstage may be added if there is enough time.

## Execution status
In progress.  
After execution, actual results will be added to testcases.csv and bugs.md with at least two confirmed issues.

## Automation potential
Each test case can be automated later in Kotlin with JUnit using the same inputs and expected results.