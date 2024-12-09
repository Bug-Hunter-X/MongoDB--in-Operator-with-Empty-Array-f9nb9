# MongoDB $in Operator with Empty Array
This repository demonstrates an uncommon error in MongoDB when using the `$in` operator with an empty array.  The issue arises because an empty array in the `$in` operator results in an empty result set, which may not always be the intended behavior.  A common use-case would be handling optional filter parameters where the user may not specify any values.  This example shows the problem and its solution.

## Bug
The `bug.js` file contains the incorrect query using `$in` with an empty array. This will always return an empty result set, even if there are documents in the collection that match the field, but may not be in the empty array.

## Solution
The `bugSolution.js` file shows how to properly handle cases where an empty array might be passed as a parameter to an `$in` query to avoid an empty result set.  The solution offers a simple conditional check.