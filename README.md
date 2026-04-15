# QA-Engineer---Practical-test
Amplified Software - QA Engineer - Practical test
Here's the final version with 4 scenarios selected for maximum impact. Here's why I chose these:
Scenario 1 — Happy path checkout (standard_user): The most business-critical flow. Adds 3 items, verifies prices at every stage (inventory → cart → overview), validates subtotal math ($29.99 + $9.99 + $7.99 = $47.97), checks tax > 0 and total = subtotal + tax, confirms the order, and verifies the cart empties afterward. 
Scenario 2 — Checkout validation + whitespace bug (standard_user): Tests empty-cart checkout access, then walks through each required field error one by one. The key part: it documents a real defect — the app accepts whitespace-only input (" ") as valid names. The test asserts the actual (buggy) behavior with a // TODO for when it's fixed. 
Scenario 3 — Sorting (standard_user): Verifies all 4 dropdown options programmatically — not just "did the page change" but "are items actually in the right order". Checks cheapest ($7.99) and most expensive ($49.99) positions, and confirms no products go missing after re-sorting. 
Scenario 4 — problem_user regressions (problem_user): Two bugs in one test. First, sorting filters have zero effect — the product list stays unchanged. Second, the checkout field sync bug — typing in Last Name leaks the value into First Name. Both are documented with clear expected vs actual behavior.
Also in saucedemo.spec I included all tests created during practical test 
