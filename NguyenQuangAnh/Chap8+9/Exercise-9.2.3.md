*__Question:__ Answer questions (a) through (d) for the mutant on line 6 in the method sum().*

!["image"](Exercise-9.2.3-image.png)

*__Answer:__*
- *a. If possible, find test inputs that do not reach the mutant.*
  <br><br> It is impossible. The mutant will always reach no matter what.<br><br>
- *b. If possible, find test inputs that satisfy reachability but not
  infection for the mutant.*
  <br><br>It is impossible. Infection will occur no matter what.<br><br>
- *c. If possible, find test inputs that satisfy infection, but not
  propagation for the mutant.*
  <br><br>If the sum of elements in x is equal to 0, then the output will be correct.
  <br>Example: x = [4, 1, -5]<br><br>
- *d. If possible, find test inputs that strongly kill the mutants.*
  <br><br>To kill the mutants strongly, all the elements in x will have the same sign (positive or negative).
  <br>Example: x = [-1, -4, -3]<br>



