# Objective-C NSManagedObjectContext Thread Safety Issue

This repository demonstrates a common error in Objective-C related to thread safety when using `NSManagedObjectContext` with Core Data.  Accessing the context from a thread other than the one it was created on can lead to crashes or data inconsistencies.

## Problem

The `bug.m` file shows an example of incorrectly accessing the `NSManagedObjectContext` from a background thread, violating thread safety rules.

## Solution

The `bugSolution.m` file demonstrates the correct approach, utilizing `performBlock:` or `performBlockAndWait:` to ensure thread safety.

This issue is crucial for developers working with Core Data in Objective-C to prevent unexpected behavior and maintain data integrity.