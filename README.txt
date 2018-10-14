### Changes
1. Converted the project to `gradle` from `ant`
2. added logback to support logging messages to file and console
3. created test classes with more wrapper iterations of underlying classes.

### Compile:
./gradlew clean build
Note: This will run all the tests and generate the results under output.
Depending on the machine, it may take long time, since in some tests, 100 or even 1000 iterations are run. Run times may be around 40 minute or so.

This creates a jar file : build/libs/abagail-1.0-SNAPSHOT.jar

### Build without test
./gradlew clean build -x test

### Data:
The scaled data is under subdirectory "data" and the file is "foo.csv"

### Output:
All the generated output is under "output".

### Tests Construction
There are 4 classes to execute various aspects of this homework.
They are under src/test/java/example
1. EyeStateTestTest
   perform neural network by replacing backpropagation with each of the four optimizers.

2. TwoColorComparisonTester

3. TSPComparisonTest

4. FourPeaksComparisonTest

### Execution:

These classes can be executed by opening in an IDE And running each class individually.
Or, we can execute them via gradle as,

./gradlew  -Dtest.single=*EyeStateTestTest test
./gradlew  -Dtest.single=*FourPeaksComparisonTest test
./gradlew  -Dtest.single=*TSPComparisonTest test
./gradlew  -Dtest.single=*TwoColorComparisonTester test

Notice the asterisk before the name of the class to wildcard the package name, since it is unconventional.
