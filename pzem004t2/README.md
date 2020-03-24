# Pzem004t2 - (for Pzem004t v1 and v2)
This custom components allows you to get the Energy data from directly from the pzem004t (v1 & v2)

Remember that the pzem provides the value in Wh so if you want to convert to kWh it is necessary to multiply the value by 0.001, in the following configuration it is also illustrated how to carry out the multiplication

YAML Example:

```yaml
sensor:
  - platform: pzem004t2
    current:
      name: "Current"
    voltage:
      name: "Voltage"
    power:
      name: "Power"
    energy:
      name: "Total Energy"
      filters:
        # Multiplication factor from Wh to kWh is 0.001
        - multiply: 0.001
      unit_of_measurement: kWh
      accuracy_decimals: 3
    update_interval: 5s
    
 ```
