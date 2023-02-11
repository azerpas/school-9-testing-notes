## Specs
- IRL: most likely incomplete and/or wrong
- Way to deal: refine reqs with the authors

## Defect
System do one of the following:
1. Not meet requirements
2. Return wrong results
3. Stop execution unexpectedly

## Testing approaches
### Black-box
- Tester has no knowledge of the internal structure of the system
- Tester acts as a user of the software
### White-box
- Tester has knowledge of the codebase and test it
### Gray-box
- Access the system as a user...
- ...but also has knowledge of the codebase

## Testing levels
### Smoke testing
- Minimal testing to ensure that the system is working for futher testing 
- e.g. e-commerce: check if the website is up, search item, add to cart
### Acceptance testing
- Testing to ensure that the system is ready for next phase of life cycle, e.g. production or delivery
#### Types of releases
- Walking skeleton: minimal viable product
- Alpha: lot of bugs expected
- Beta: new features and fewer bugs, bigger audience
- Release candidate: promoting betas
- Public release: promoting a release candidate
### Exploratory testing
- Testing without **a specified test plan**
- Learn about and influence the dev of the system
### A/B Testing
- Testing by comparing two versions of the system to see which one performs better to the user
### Penetration testing
- Testing to find vulnerabilities in the system

## Manual vs. Automated testing
### Manual testing
| Pros | Cons |
| --- | --- |
| It's simple | It's boring |
| It's cheap | It's often not repeatable |
| Easy to set up | Some tasks are difficult manually |
| It's flexible | It's time consuming |
| Most likely catch humans errors | Black/gray-box only |

### Automated testing
| Pros | Cons |
| --- | --- |
| No human error | Setup time |
| Repeatable | Need skilled people |
| Simple to analyze results | Only test for what they were designed for |