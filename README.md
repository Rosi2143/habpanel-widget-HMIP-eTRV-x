# habpanel-widget-HMIP-eTRV-x
HAB-Panel widget for all HMIP-eTRV devices.
It has been tested with 
* HmIP-eTRV-2
* HmIP-eTRV-C
but should also work with
* HmIP-eTRV
* HmIP-eTRV-B

# usage
the widget uses a "generic item element" that is the common part of the name of expected elements
* <generic>_TempSet == 1#SET_POINT_MODE
* <generic>_TempAct == 1#ACTUAL_TEMPERATURE
* <generic>_WindowState == 1#WINDOW_STATE
* <generic>_BatteryStatus == 0#LOW_BAT
* <generic>_UpdatePending == 0#UPDATE_PENDING
* <generic>_PartyMode == 1#PARTY_MODE
* <generic>_BoostTime == 1#BOOST_TIME
* <generic>_Profile == 1#ACTIVE_PROFILE
  
  e.g. I defined these items for one eTRV-2
* Number ThermostatBad_TempSet
* Number ThermostatBad_TempAct
* String ThermostatBad_WindowState
* Switch ThermostatBad_BatteryStatus
* Switch ThermostatBad_UpdatePending
* Switch ThermostatBad_PartyMode
* Number ThermostatBad_BoostTime
* Number ThermostatBad_Profile

