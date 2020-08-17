# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given Sensor turn on
  When Patient show their card
  And check the date 
  And add patient in working days or holiday record 
  Then Director can see "number of patient visit on working days or holidays"

Scenario: Compute parking slots to reserve for visiting specialists

  Given Sensor turn on and reserve some slots 
  When Check reserve slot count greater than one
  and decrement reserve slot count by one
  Then Director can see "slot is free or not"
