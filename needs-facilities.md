# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given Camera and sensor turned on
  When  VisitorCount+=1
  Then I see "number of visitors"

Scenario: Alert when seating capacity is full

  Given Sensor is turned on
  When Count the vacant chair.
  Then I see "chair is vacant or not".
