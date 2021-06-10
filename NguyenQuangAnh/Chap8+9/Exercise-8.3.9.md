*__Question:__ For the Quadratic program in Chapter 7, complete the test sets for the following coverage criteria by filling in the “don’t care” values. Make sure to ensure reachability. Then derive the expected output. Download the program, compile it, and run it with your resulting test cases to verify
correct outputs.*

(a) Predicate Coverage (PC)<br>
(b) Clause Coverage (CC)<br>
(c) Combinatorial Coverage (CoC)<br>
(d) Correlated Active Clause Coverage (CACC)<br>

*__Answer:__*
We use the same test sets for all 4 Coverages:

```Java
import org.junit.Test;
import static org.junit.Assert.*;

public class TestQuadratic {
    @Test
    public void test_root()
    {
        assertTrue(Quadratic.Root(1, -8, 16));
        assertTrue(Quadratic.Root(1, -5, 5));
        assertFalse(Quadratic.Root(1, -1, 1));
    }
}
```


