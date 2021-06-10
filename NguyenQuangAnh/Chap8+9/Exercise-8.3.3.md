*__Question:__ Complete and run the tests to satisfy CACC for the Thermostat
class.*

*__Answer:__*
```Java
import org.junit.Test;
import static org.junit.Assert.*;
import java.io.*;
import java.util.*;
public class TestThermostat
{
	@Before
	public void init(){
		Thermostat ts = new Thermostat();
		ProgrammedSettings s = ProgrammedSettings();
		s.setSetting(Period.MORNING, DayType.WEEKDAY, 69);
    		ts.setPeriod(Period.MORNING);
    		ts.setDay(DayType.WEEKDAY);
	}
	@Test // Ttft
	public void test_a_true(){
		ts.setCurrentTemp(63);
    		ts.setThresholdDiff(5);
    		ts.setOverride(true);
	    	ts.setOverTemp(60);
    		ts.setMinLag(10);
    		ts.setTimeSinceLastRun(12);
    		assertTrue(ts.turnHeaterOn(s));
	}
	@Test // Ftft
	public void test_a_false(){
		ts.setCurrentTemp(70);
    		ts.setThresholdDiff(5);
    		ts.setOverride(true);
	    	ts.setOverTemp(60);
    		ts.setMinLag(10);
    		ts.setTimeSinceLastRun(12);
    		assertTrue(ts.turnHeaterOn(s));
	}
	@Test // fTtt
	public void test_b_true(){
		ts.setCurrentTemp(70);
    		ts.setThresholdDiff(5);
    		ts.setOverride(true);
	    	ts.setOverTemp(90);
    		ts.setMinLag(10);
    		ts.setTimeSinceLastRun(12);
    		assertTrue(ts.turnHeaterOn(s));
	}
	@Test // fFtt
	public void test_b_false(){
		ts.setCurrentTemp(70);
    		ts.setThresholdDiff(5);
    		ts.setOverride(false);
	    	ts.setOverTemp(90);
    		ts.setMinLag(10);
    		ts.setTimeSinceLastRun(12);
    		assertTrue(ts.turnHeaterOn(s));
	}
	@Test // tttT
	public void test_d_true(){
		ts.setCurrentTemp(63);
    		ts.setThresholdDiff(5);
    		ts.setOverride(true);
	    	ts.setOverTemp(70);
    		ts.setMinLag(10);
    		ts.setTimeSinceLastRun(12);
    		assertTrue(ts.turnHeaterOn(s));
	}
	@Test // tttF
	public void test_d_false(){
		ts.setCurrentTemp(63);
    		ts.setThresholdDiff(5);
    		ts.setOverride(true);
	    	ts.setOverTemp(70);
    		ts.setMinLag(15);
    		ts.setTimeSinceLastRun(12);
    		assertTrue(ts.turnHeaterOn(s));
	}
}
```