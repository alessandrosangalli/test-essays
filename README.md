# test-essays

Four good attributes:
1 - Protect against regression (mutually exclusive) (negotiable)
2 - Resistance to refactoring (mutually exclusive) (non-negotiable)
3 - Fast feedback (mutually exclusive) (negotiable)
4 - Maintainability

Value of tests = value of each 4 attributes.
If one attribute goes to zero, the total is zero.
You can maximize only 2 of the 3 because 1, 2 and 3 are mutually exclusive

Test coverage targets are bad because:
1 - Unit testing is not "the more the better"
2 - Unnecessary and poorly written tests generate unnecessary cost

Tests are not a free resource. It is not possible to say a percentage of correct code coverage for a system, when you force people to write tests to achieve a goal you have the following expense:

Time spent writing test that does not add value
+
Test maintenance time spent during the system lifecycle (poorly written test generates frequent maintenance and the more tests, mainly unnecessary, the greater the chance of having tests coupled to the code), this avoids refactoring and continuous improvement (because tests break when refactoring rather than only breaking when there is a change in behavior).

It's better to teach people how to test intelligently, spending little resources and earning a lot of reward (in this case it's controlling the entropy of the software during its lifecycle).

Test exists to reduce entropy.

Tests in the application domain are generally the ones that create the most value.

Test coverage are a good negative (not positive) indicator.

Generally in-domain tests tend to be more classic and out-of-domain tests tend to be more mockists.

Tests that fail for no reason decrease your ability to react to problems. They often cause confidence in test suites to decrease, making you think that every time a test breaks it's because it was refactored. You stop view your test suite as a reliable feedback source.

Test is for testing behavior, refactoring doesn't change behavior, so tests shouldn't break because of refactoring.

Refactoring is extremely underrated and very important, without good testing we will not have continuous refactoring.

You might think that testing mediocre is at least doing something, but bad test suites in extreme cases can be worse than not testing at all. We must strive for excellence in testing and not accept poor quality.

If you can't trace a test to a business requirement - remove it, except in utility code with high algorithmic complexity.
