# Kotlin Nullable List map() Function Issue

This repository demonstrates an uncommon issue encountered when using the `map()` function on nullable lists in Kotlin.  The `map()` function, when applied to a null list, returns `null` instead of an empty list, which can cause unexpected null pointer exceptions if not handled properly.

## Problem

When working with nullable lists in Kotlin, using the `map()` function directly on a nullable list that could potentially hold a null value will lead to the function returning `null`. This is counterintuitive as one might expect an empty list in such cases.

## Solution

The solution involves using the safe call operator (`?.`) along with the Elvis operator (`?:`) to provide a default empty list when the nullable list is null. This ensures that the `map()` function always operates on a non-null list, preventing potential null pointer exceptions.

## How to reproduce

1. Clone this repository.
2. Run `bug.kt` to observe the issue.
3. Then, run `bugSolution.kt` to see the correct way to handle nullable lists with `map()`.