*__Question:__ For the index() program in Chapter 7, complete the test sets for
the following coverage criteria by filling in the “don’t care” values. Make sure to ensure reachability. Then derive the expected output. Download the program, compile it, and run it with your resulting test cases to verify correct outputs.*

(a) Predicate Coverage (PC)<br>
(b) Clause Coverage (CC)<br>
(c) Combinatorial Coverage (CoC)<br>
(d) Correlated Active Clause Coverage (CACC)<br>

*__Answer:__*
We use the same test sets for all 4 Coverages:

```Java
import org.junit.Test;

import static org.junit.Assert.assertEquals;

public class Test_PatternIndex {
    @Test
    public void test_patterIndex_found()
    {
        assertEquals(PatternIndex.patternIndex("hello", "ell"), 1);
    }
    
    @Test
    public void test_patternIndex_emptyString()
    {
        assertEquals(PatternIndex.patternIndex("hello", ""), -1);
        assertEquals(PatternIndex.patternIndex("", "ell"), -1);

    }
    
    @Test
    public void test_patternIndex_notFound()
    {
        assertEquals(PatternIndex.patternIndex("hello", "hellooo"), -1);
    }
}
```