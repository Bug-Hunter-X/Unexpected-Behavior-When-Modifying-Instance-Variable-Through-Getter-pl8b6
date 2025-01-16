# Ruby Instance Variable Modification Bug

This repository demonstrates an uncommon bug in Ruby related to modifying instance variables indirectly through getter methods.  The code shows that attempting to assign a new value using the getter method does not change the actual instance variable's value. This is because the getter method simply returns a copy of the value, not a reference to the instance variable itself.

The solution demonstrates how to correctly modify instance variables, emphasizing the importance of explicitly assigning to the `@instance_variable` rather than trying to change its value via the getter.

## Bug

The `bug.rb` file showcases the problematic code.  Note that assigning a new value via the `value` method (which is simply a getter) does not affect the internal `@value` instance variable.

## Solution

The `bugSolution.rb` file provides the corrected approach. The instance variable is directly modified using the `@value` notation.