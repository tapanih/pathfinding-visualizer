## Week 1

Work time: 11 hours

I wrote the project specification. This involved a lot of reading about different pathfinding algorithms. I tried to figure out all the time and space complexities and what data structures and operations each algorithm requires.  Djikstra's algorithm and A* are straight-forward to implement but jump point search looks slightly complicated, especially with diagonal movements. Fringe search is something I stumbled upon while doing research but I probably won't have time to implement it. It should be faster than A* according to this publication: http://www.ru.is/faculty/yngvi/pdf/BjornssonEHS05.pdf

I created a Gradle project for the program and tried to do as much of the configuration as possible. I set up Jacoco for code coverage and Checkstyle for style checking. For Checkstyle, I elected to use Google Style Guide as it looked reasonable based on the documentation. I set up GitHub Actions for automatically creating code coverage reports and sending them to codecov.io.

I also found about commons-cli library that provides utilities for parsing command line options and also generates help messages. Adding it in to
the project proved to be somewhat difficult because I am not very familiar with Gradle. Eventually I did manage to get it working.

I wrote a crude parser for the map files provided by Moving AI Labs with simple unit tests. It doesn't support all the map features yet but should be enough to get started. The scenario files would make testing quite straight-forward so a parser for them would be nice as well. The solutions given assume a diagonal cost of sqrt(2) though. This value can be hard coded as a constant but still requires the program to use floating-point numbers.

Next week I am going to start implementing path-finding algorithms using data structures from the Java library.

