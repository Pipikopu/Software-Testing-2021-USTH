*__Question:__ Complete and run the tests to satisfy CC for the Thermostat
class.*

*__Answer:__*

```Java
public class TestThermostat
{
  @Test
  public void testCC()
  {
    Thermostat t = new Thermostat();
    ProgrammedSettings s = new ProgrammedSettings();

    s.setSetting(Period.MORNING, DayType.WEEKDAY, 70);
    t.setPeriod(Period.MORNING);
    t.setDay(DayType.WEEKDAY);

    t.setCurrentTemp(64);
    t.setThresholdDiff(5);

    t.setCurrentTemp(68);
    t.setThresholdDiff(5);

    t.setOverride(true);
    t.setOverride(false);

    t.setOverTemp(74);
    t.setOverTemp(65);

    t.setMinLag(10);
    t.setTimeSinceLastRun(12);

    t.setMinLag(10);
    t.setTimeSinceLastRun(5);

    assertTrue(t.turnHeaterOn(s));
  }
}
```