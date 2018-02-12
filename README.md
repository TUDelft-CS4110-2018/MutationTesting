# Mutation Testing

Mutation testing is a fault seeding approach that is used to evaluate the quality of an existing test suite. It can also 
potentially be used to guide the test creation process.

A frequently used and rather well-known approach to give a (superficial) indication of test quality are the various structural coverage metrics, e.g., branch coverage. Many IDEs either offer these metrics directly or through a plug-in. But whether you write 1 test or a thousand, your coverage can be identical. The diagnostic power of these two very different scenarios is however not the same.

As said, mutation testing introduces defects into the production code, by making small alterations. These alterations are made by applying so-called mutation operators. An easy to understand operator changes a "+" operator into a "-" operator in mathematical expressions.

What could now happen?
   * There is a test that covers the expression and the test fails --> the mutant is killed.
   * There is no test that covers the expression or the test doesn't catch the defect --> the mutant survives.
   * The end-result of the computation is identical, even though the mutation operator was applied --> mutant equivalence problem
   
What should you try to do? 
1. Take an old school project written in Java that has jUnit tests. If you don't have any lying around, look around on GitHub :-)
2. Download PITest (http://pitest.org).
3. Apply PITest on your application.
4. Report on what you see in terms of coverage and in terms of mutation score.
5. Repeat with more projects.

Finally, put everything into context by also reading the following papers:
1. Laura Inozemtseva, Reid Holmes: Coverage is not strongly correlated with test suite effectiveness. ICSE 2014: 435-445
2. René Just, Darioush Jalali, Laura Inozemtseva, Michael D. Ernst, Reid Holmes, Gordon Fraser: Are mutants a valid substitute for real faults in software testing? SIGSOFT FSE 2014: 654-665
