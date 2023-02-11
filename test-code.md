# Production|Test code
## Production code
Used by final user
### Example
```java
/* Production code */
class Calculator {
    public static int add4(int x) {
        return x + 4;
    }
}
```

### Test code
Used by developers to test the production code
### Example
```java
class CalculatorTests {
    @Test
    public void add_four_to_one_returns_five() {
        int actual = Calculator.add4(1);
        int expected = 5;
        assertEquals(expected, actual);
    }
}
```

# Test code analysis
- Tests are often in a separate file/package
- **Test case**: a collection of tests
- **Test suite**: a collection of test cases

## Anatomy of a test
```java
@Test
// ↓Name
void can_book_one_seat_when_train_is_empty() {
    // Arrange
    var train = Helpers.makeEmptyTrain(100);
    var booking = new Booking(train);
    // Act
    var seatNumber = booking.book(1);
    // Assert
    assertTrue(train.getSeat(seatNumber).isOccupied());
}
```

# Continous integration
## CI Scripts
CI scripts are used to automate:
- Building
- Testing
- Packaging
- Deploying
- Etc...
#### They can
- Run on a schedule
- Run upon certain events (e.g. push to a branch)
- Run manually

### Coordinator
- A coordinator is a program that listens to triggers above
- It then runs the CI script
- Aggregates the results

### Job
Script + Configuration

### Build
Execution of a job

### Step
- Fetch code
- Compile
- Run tests

### Artifact
A file produced by a step

### Delivery
An artifact that is delivered to a customer

### Deployment 
Upload an artifact to a server

<img width="477" alt="image" src="https://user-images.githubusercontent.com/19282069/218268984-8025d8be-f503-4172-b367-e91386e0279a.png">

## Examples
- Jenkins
- GitHub Actions
- GitLab CI

# Coverage
**Goal**: to ensure that the test cases cover all the code
- Try to keep the coverage as high as possible (>80%)
- Too hard (>80%)? Just don't
- Take a look at the coverage report frequently

# Test limitations
- Test code is not human, it can't think
- Not enough assertions gives false confidence
- False positives: test fails when it shouldn't, *annoying*
- False negatives: test passes when it shouldn't, *a  lot worse*
- Flakyness: fails once in a while, need to be dealt with