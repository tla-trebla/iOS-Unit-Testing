# iOS-Unit-Testing
This tutorial is based on tutorial named iOS Unit Testing and UI Testing Tutorial by Ray Wenderlich. 
Link: https://www.raywenderlich.com/21020457-ios-unit-testing-and-ui-testing-tutorial#toc-anchor-017

# Things I've Learned
* Things to consider on what to test:
  * Individual part without dependency (state-based testing).
  * How each part works together in real-life environment (integration testing).
  * UI testing.
  * Bug fix.
* Separate unit tests into different targets between state-based testing & slow testing (asynchronous).
* Asynchronous should use `expectation` for what condition to make the test passed and `fulfill` if the expectation met.
* Instead of waiting the `expectation` showing an error, we can overcome it by check from the `dataTask`'s error response if there's.
* Skip test with `XCTSkip` if there's issue that can't be fulfilled (example: network connection).
* Separate fake tests into different class with same target as state-based testing.
* Create fake object marked by `stub` on the last name to provide an input.
* Create fake class marked by `mock` on the first name to not using a genuine class.
* In UI testing, it's better to declare the recorded UI objects as a variables.
* When measuring the performance of tested code, mark the test name with `Performance` on the last.
* There are bunch of metrics to check, generally there's:
  * XCTClockMetric: how much time elapsed.
  * XCTCPUMetric: monitors CPU in time, cycles, number of command.
  * XCTStorageMetric: how many storage has been stored from tested code.
  * XCTMemoryMetric: monitors physical memory used.
* Enable code coverage from `Edit Scheme > Test > Options` then check `Gather coverage for all targets`.
  * Some say 85 to 90 percent coverage is better because those 15 or 10 percent coverage are hard to get.
  * Some say those hard to get coverage indicates there's a anti-pattern code.
  
# Questions I've Had
* How to create `stub` or `mock`?
* How do I read performance test results?
* What's an anti-pattern code?
* Any other metrics I should be aware of?
