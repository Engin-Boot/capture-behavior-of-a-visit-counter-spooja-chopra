# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given System count visit-counter
  When server crash or down
  Then restart the server

Scenario: Reconcile counts if the sensor is offline for a while

  Given Sensor is turn on
  When Sensor is offline
  Then Reconcile count
