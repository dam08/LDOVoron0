# VIS PLATEAU (BED_SCREWS_ADJUST)
## Lancer le nivellement
### Mise en chauffe
    SET_HEATER_TEMPERATURE HEATER=heater_bed TARGET=105
    SET_HEATER_TEMPERATURE HEATER=extruder TARGET=200
### Buse au centre du plateau
    G28
## Premier reglage du Z-Offset
    Z_ENDSTOP_CALIBRATE
### Ajustement des vis du plateau
    BED_SCREWS_ADJUST
## Second ajustement du Z-Offset
    Z_ENDSTOP_CALIBRATE
### Ajustement avec une feuille de papier
    TESTZ Z=-0.1
### Valider la valeur
    ACCEPT
### Sauvegarder la configuration (z_position_endstop)
    SAVE_CONFIG