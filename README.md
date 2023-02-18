# InkBird-Thermometer

template:

  - sensor:
      - name: "BBQ Temp Sensor State"
        state: >
          {% if states('sensor.ibbq_982f_temperature_probe_1') == "unavailable" %}
            Powered Off
          {% else %}
            Powered On
          {% endif %}

  - sensor:
      - name: "BBQ Temp Sensor 1"
        unique_id: sensor.bbq_temp_sensor_1
        unit_of_measurement: °F
        state: >
          {% if states('sensor.ibbq_982f_temperature_probe_1') == "32" %}
            Off
          {% elif states('sensor.ibbq_982f_temperature_probe_1') == "unavailable" %}
            Off 
          {% else %}
            {{ states('sensor.ibbq_982f_temperature_probe_1') }}
          {% endif %}
          
  - sensor:
      - name: "BBQ Temp Sensor 2"
        unique_id: sensor.bbq_temp_sensor_2
        unit_of_measurement: °F
        state: >
          {% if states('sensor.ibbq_982f_temperature_probe_2') == "32" %}
            Off
          {% elif states('sensor.ibbq_982f_temperature_probe_2') == "unavailable" %}
            Off 
          {% else %}
            {{ states('sensor.ibbq_982f_temperature_probe_2') }}
          {% endif %}
 
  - sensor:
      - name: "BBQ Temp Sensor 3"
        unique_id: sensor.bbq_temp_sensor_3
        unit_of_measurement: °F
        state: >
          {% if states('sensor.ibbq_982f_temperature_probe_3') == "32" %}
            Off
          {% elif states('sensor.ibbq_982f_temperature_probe_3') == "unavailable" %}
            Off 
          {% else %}
            {{ states('sensor.ibbq_982f_temperature_probe_3') }}
          {% endif %}	 
  - sensor:
      - name: "BBQ Temp Sensor 4"
        unique_id: sensor.bbq_temp_sensor_4
        unit_of_measurement: °F
        state: >
          {% if states('sensor.ibbq_982f_temperature_probe_4') == "32" %}
            Off
          {% elif states('sensor.ibbq_982f_temperature_probe_4') == "unavailable" %}
            Off 
          {% else %}
            {{ states('sensor.ibbq_982f_temperature_probe_4') }}
          {% endif %}                    
