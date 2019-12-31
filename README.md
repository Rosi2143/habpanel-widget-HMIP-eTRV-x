# habpanel-widget-HMIP-eTRV-x
HAB-Panel widget for all HMIP-eTRV devices.
It has been tested with 
* HmIP-eTRV-2
* HmIP-eTRV-C

but should also work with
* HmIP-eTRV
* HmIP-eTRV-B

# usage
the widget uses a 
## "generic item element"

This config parameter is used to access further items with a defined naming pattern.
This should make it easier to set up a whole bunch of widgets

The common part of the name of expected items is defined in the config pannel and the real items are derived in an item file.

| name                     | channel number#NAME   | example                              |
|--------------------------|-----------------------|--------------------------------------|
| <generic>_BatteryStatus  | 0#LOW_BAT             | `Switch ThermostatBad_BatteryStatus` |
| <generic>_UpdatePending  | 0#UPDATE_PENDING      | `Switch ThermostatBad_UpdatePending` |
| <generic>_TempSet        | 1#SET_POINT_MODE      | `Number ThermostatBad_TempSet`       |
| <generic>_TempAct        | 1#ACTUAL_TEMPERATURE  | `Number ThermostatBad_TempAct`       |
| <generic>_WindowState    | 1#WINDOW_STATE        | `String ThermostatBad_WindowState`   |
| <generic>_PartyMode      | 1#PARTY_MODE          | `Switch ThermostatBad_PartyMode`     |
| <generic>_BoostTime      | 1#BOOST_TIME          | `Number ThermostatBad_BoostTime`     |
| <generic>_Profile        | 1#ACTIVE_PROFILE      | `Number ThermostatBad_Profile`       |

e.g.
```
Switch  ThermostatBad_BatteryStatus       "Thermostat Bad Batterie [%s]"              {channel="homematic:HmIP-eTRV-2:3014F711A061A7D70992B1AC:000A1709A651A7:0#LOW_BAT" }
Switch  ThermostatBad_UpdatePending       "Thermostat Bad Update [%s]"                {channel="homematic:HmIP-eTRV-2:3014F711A061A7D70992B1AC:000A1709A651A7:0#UPDATE_PENDING" }
Number  ThermostatBad_TempSet             "Thermostat Bad Temperatur Set [%.1f]°C"    {channel="homematic:HmIP-eTRV-2:3014F711A061A7D70992B1AC:000A1709A651A7:1#SET_POINT_TEMPERATURE" }
Number  ThermostatBad_TempAct             "Thermostat Bad Temperatur Act [%.1f]°C"    {channel="homematic:HmIP-eTRV-2:3014F711A061A7D70992B1AC:000A1709A651A7:1#ACTUAL_TEMPERATURE" }
String  ThermostatBad_WindowState         "Thermostat Bad Window [%s]"                {channel="homematic:HmIP-eTRV-2:3014F711A061A7D70992B1AC:000A1709A651A7:1#WINDOW_STATE" }
Switch  ThermostatBad_PartyMode           "Thermostat Bad Party Active [%s]"          {channel="homematic:HmIP-eTRV-2:3014F711A061A7D70992B1AC:000A1709A651A7:1#PARTY_MODE" }
Number  ThermostatBad_BoostTime           "Thermostat Bad Remaining Boost time [%d]"  {channel="homematic:HmIP-eTRV-2:3014F711A061A7D70992B1AC:000A1709A651A7:1#BOOST_TIME" }
Number  ThermostatBad_Profile             "Thermostat Bad WeekProgramm [%s]"          {channel="homematic:HmIP-eTRV-2:3014F711A061A7D70992B1AC:000A1709A651A7:1#ACTIVE_PROFILE" }
```
## minimum and maximum temperature
here you set the minimum and maximum temperature that can be set for this device. It is used to limit the SetTemp boundaries.
These are just pure numbers - they depend on how your device is set up.
So if you use °C or °F your numbers will be °C or °F respectively.

## profile names
you can choose 3 profiles (at least with the eTRV-2 and eTRV-C devices). If you want to assign names to the profiles for better understanding - this is the place to do it. I have define 3 profiles
* normal
* vacation (we are there all day)
* absense (we are gone all day)

# examples and usage
## small
![alt text](https://github.com/Rosi2143/habpanel-widget-HMIP-eTRV-x/blob/master/eTRV-2_2.jpg "small widget")
shows the miniumum version of the widget.

## normal
![alt text](https://github.com/Rosi2143/habpanel-widget-HMIP-eTRV-x/blob/master/eTRV-2_1.jpg "normal widget")

## setting temperature
![alt text](https://github.com/Rosi2143/habpanel-widget-HMIP-eTRV-x/blob/master/eTRV-2_3.jpg "set temperature")
any press on the TempSet items opens a slider to set the temperature.
