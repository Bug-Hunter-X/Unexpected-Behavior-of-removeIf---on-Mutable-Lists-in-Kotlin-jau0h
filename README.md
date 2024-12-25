# Unexpected Behavior of removeIf() on Mutable Lists in Kotlin

This repository showcases a common pitfall when using the `removeIf()` function on mutable lists in Kotlin.  The example demonstrates how the internal iterator used by `removeIf()` can skip elements when removing elements based on a condition.

The `bug.kt` file contains the erroneous code.  The `bugSolution.kt` file offers a corrected version.

This issue arises because the iterator advances even when an element is removed, potentially skipping elements that would otherwise satisfy the removal condition.