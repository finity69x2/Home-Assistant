Place the following in your "resources" section in your lovelace configuration:

  ``- url: /local/lovelace/fan-control-entity-row.js
    type: js
  ``
    
Then to use this in a card place the following in your entity card:
    
  ``- type: entities
    title: Sunroom
    show_header_toggle: false
    entities:
      - switch.sunroom_light
      - entity: fan.sunroom_fan
        type: custom:fan-control-entity-row
        name: Sunroom Fan    
  ``
