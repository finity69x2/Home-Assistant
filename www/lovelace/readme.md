Place the following in your "resources" section in your lovelace configuration:

  ```
    - url: /local/lovelace/fan-control-entity-row.js
      type: js
  ```
    
Then to use this in a card place the following in your entity card:
    
  ```
  cards:
    - type: entities
        title: Fans
        show_header_toggle: false
        entities:
        ## USE THIS CONFIG TO HAVE IT MATCH YOUR THEME ##
          - entity: fan.master_bedroom_fan
            type: custom:fan-control-entity-row
            name: MBR Fan Not Custom
            customTheme: false
        ## USE THIS CONFIG TO USE A DEFAULT CUSTOM THEME
          - entity: fan.sunroom_fan
            type: custom:fan-control-entity-row
            name: Sunroom Fan Default Custom
            customTheme: true
        ## USE THIS CONFIG TO USE A 'CUSTOMZED' CUSTOM THEME
          - entity: fan.sunroom_fan
            type: custom:fan-control-entity-row
            name: Sunroom Fan Custom Custom
            customTheme: true
            customIsOnLowColor: 'rgb(255, 0, 0)'
            customIsOnMedColor: '#888888'
            customIsOnHiColor: '#222222'
            customIsOffSpdColor: '#aaaaaa'
            customIsOffColor: 'purple'
  ```

This is with the default Lovelace frontend theme set:


This is with the "Slate" frontend theme set:
