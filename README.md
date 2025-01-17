# COBOL Shallow Copy Bug

This example demonstrates a potential issue with the `MOVE` statement in COBOL when dealing with complex data structures.  The `MOVE` statement, when used with complex data structures, performs a shallow copy instead of a deep copy.  This can lead to unexpected behavior if one of the structures is modified after the copy operation.

## Bug Description

The `bug.cob` file shows a simple program. The `MOVE` statement does not create an independent copy of the data; therefore, changes made to the original structure will also affect the copy.

## Solution

The `bugSolution.cob` file provides a solution to avoid this issue using the `MOVE CORRESPONDING` statement for complex data structures. For simpler data structures, explicit field-by-field assignments ensure independent copies are created.