# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays
  Given Sensor turn on
  When Patient show their card
    And check the date
    And add patient in working days or holiday record
  Then Director can see "number of patient visit on working days or holidays".
  
Scenario: Compute parking slots to reserve for visiting specialists

  Given Sensor is turn on and set number of reserve slots.
  When Check reserve slots count and decrement it.
  Then I see "slot is free or not".
