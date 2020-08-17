# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given Camera and sensor turn on
  When  Count Visitor and update
  Then I see "number of visitors"

Scenario: Alert when seating capacity is full

  Given Sensor is turn on
  When Count the vacant chair.
  Then I see "chair is vacant or not".
