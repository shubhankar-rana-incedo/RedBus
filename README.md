# RedBus

REDBUS.feature
Feature: Find total zing bus

@bus
  Scenario Outline: total Zing busses

    Given Visit redbus.in
    When Search bus "<from>" "<to>"
    Then Select date of journey and click search busses
    When We select AC and After 6 pm 
    And Select Live Tracking
    Then Count the number of Zing busses

    Examples:
        | from  | to         |
        | Delhi | Chandigarh |
