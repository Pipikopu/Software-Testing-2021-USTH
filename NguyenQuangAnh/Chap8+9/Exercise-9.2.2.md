*__Question:__ Answer questions (a) through (d) for the mutant on line 5 in the method findVal().*

!["image](Exercise-9.2.2-image.png)

*__Answer:__*
<br><br>
- *a. If possible, find test inputs that do not reach the mutant.*
  <br><br> It is impossible. The mutant will always reach no matter what.<br><br>
- *b. If possible, find test inputs that satisfy reachability but not
  infection for the mutant.*
  <br><br>It is impossible. Infection will occur no matter what.<br><br>
- *c. If possible, find test inputs that satisfy infection, but not
  propagation for the mutant.*
  <br><br>If the last occurrence of _val_ is not equal to _numbers[0]_, then the output will be correct. 
  <br>Example: (numbers, val) = ([2, 3], 3)<br><br>
- *d. If possible, find test inputs that strongly kill the mutants.*
<br><br>To kill the mutants strongly, the _val_ will have to occur in _numbers[0]_ only. 
  <br>Example: (numbers, val) = ([2, 3], 2)<br>

