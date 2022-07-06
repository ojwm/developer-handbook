<!-- markdownlint-disable MD033 -->
# Code Review

![code review](/images/code-review.jpeg)\
<sup>Image credit: [Unknown](https://knowyourmeme.com/memes/is-this-a-pigeon).</sup>

## Conducting a code review

Code reviews can be performed independently but are often quicker and more thorough if performed along with the developer(s) of the code.

## Comments

When making comments on code, either in person or in a source code control system, consider whether the comment is justified based on the team's agreed ways of working.

Also make a recommendation of how to change the code and indicate whether the change needs to be made before the code review is completed.\
One way of indicating this is with the [MoSCoW method](https://en.wikipedia.org/wiki/MoSCoW_method).\
For example
> SHOULD change this code to use a better pattern.

## Definition of done

Use the [definition of done](/pages/definition-of-done.md) to determine whether the code does what it needs to do.

## Branch

* Branch name conforms to the [branching strategy](/pages/branching-strategy.md).

## Build

* [Build](/pages/build.md) passes.

## Tests

The following [tests](/pages/testing.md) pass, where applicable, which may be part of the aforementioned [build](#build).

* Unit tests.
* Regression tests.
* Integration tests.
* Accessibility tests.
* Performance tests.
* Penetration tests.
* Manual tests.

## Code quality

* Code conforms to agreed [standards](/pages/code-quality.md).
* Code passes any code quality checks, which may be part of the aforementioned [build](#build).

## Security

* Code passes any [security](/pages/security.md) scans.

## Documentation

* [Documentation](/pages/documentation.md) has been completed, as necessary.

## Good enough

Code should be good enough to pass the [definition of done](/pages/definition-of-done.md). Beyond a certain point, improvements to the code do not deliver further value and time would be better spent moving on to the next task.

![good enough](/images/good-enough.jpg)
<sup>Image credit: Unknown.</sup>
