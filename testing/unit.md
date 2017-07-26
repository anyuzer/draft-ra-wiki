# Unit testing

## Why

When designing or implementing a feature, we want to know that we are doing it properly. Once the feature is implemented, we want to ensure that it keeps working.

## What

As part of our [Continuous Integration](../delivery/continuous-integration.md) practices, we are pushing for Test Driven Development, where unit tests are written BEFORE a new feature. It falls in line with the construction proverb: "measure twice, cut once".

By writing the test first:

- Ensures the code is loosely coupled
- Your code evolves in small steps
- You get automated regression testing
- You get living documentation as to how the system works
- etc.

## How

- Start with your test first, to ensure that the test fails
- Implement the feature that makes the test pass
- Avoid [fragile tests](https://www.youtube.com/watch?v=URSWYvyc42M) and tight coupling

## Who

@delivery @qa

## References

- [Magic tricks of unit testing](https://www.youtube.com/watch?v=URSWYvyc42M) _Ruby, but excellent concepts_