## Finding time for testing
>I’m going to add some tests first before adding this new feature. This means the feature will be ready in two weeks instead of one, but it will be worth it, I promise!   

*You*

> Why? It’s a waste of time! I don’t pay you to write tests, I pay you to add features.  

*Your boss*

Easier to see time spent on testing as a cost rather than an investment. But it’s an investment that pays off in the long run.

### Say this instead
> The feature will be ready in two weeks
- The way you add features is up to you

## Make good tests
Before designing a feature, meet with:
- The stakeholder
- The developer
- The tester

### Gherkin example
```gherkin
Scenario: Making a deposit
    Given I have a bank account with a balance of 200
    When I make a deposit of 50
    Then my bank account has a balance of 250
```

## CI by humans
### Positive feedback loop
- CI works well
- More tests are written
- More checks are done
- Less bugs are found
### Negative feedback loop
- CI is too long or unreliable
- Less tests are written
- CI failures are ignored
- More bugs are found
### Failing jobs
- Fix them ASAP
- Should stop creating new features to solve these
### Notifications
Make sure everyone is notified when a job fails and react accordingly
### Keep tests clean
- Readable
- Useful
- Rather short
### Keep tests independent
- Use discipline
- Execute them in order