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
| name                     | channel number#NAME   | example |
|--------------------------|-----------------------|---------|
| <generic>_TempSet        | 1#SET_POINT_MODE      | `Number ThermostatBad_TempSet` |
| <generic>_TempAct        | 1#ACTUAL_TEMPERATURE  | `Number ThermostatBad_TempAct` |
| <generic>_WindowState    | 1#WINDOW_STATE        | `String ThermostatBad_WindowState` |
| <generic>_BatteryStatus  | 0#LOW_BAT             | `Switch ThermostatBad_BatteryStatus` |
| <generic>_UpdatePending  | 0#UPDATE_PENDING      | `Switch ThermostatBad_UpdatePending` |
| <generic>_PartyMode      | 1#PARTY_MODE          | `Switch ThermostatBad_PartyMode` |
| <generic>_BoostTime      | 1#BOOST_TIME          | `Number ThermostatBad_BoostTime` |
| <generic>_Profile        | 1#ACTIVE_PROFILE      | `Number ThermostatBad_Profile` |

