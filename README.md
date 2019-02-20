# UnitTestPerf

Some projects used to demonstrate the performance of different unit testing frameworks for .NET Core.

Currently includes xUnit and NUnit. There are 1000 tests per project (despite the names saying 10k...).

## Test Results

19 Feb 2019 running VS 2017 v15.9.7
From a fresh start (launch VS, open project, Test -> Run All Tests)

**Test Discovery Times (seconds)**

```
Framework   1        2        3        Avg
NUnit       2.846    1.946    1.946    2.25
xUnit       2.988    2.177    2.261    2.48   10% longer
Diff        0.142    0.231    0.315    0.23
```

**Test Run Time (seconds)**

```
Framework   1        2        3        Avg
NUnit       1.658    1.353    1.343    1.45
xUnit       1.828    1.769    1.864    1.82   25% longer
Diff        0.170    0.416    0.521    0.37
```

Currently the difference between xUnit and NUnit from a fresh start is 600ms longer for xUnit for 1000 tests. This shouldn't be noticeable under most circumstances, especially where tests are actually performing real work.


