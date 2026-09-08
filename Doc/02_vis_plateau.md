# VIS PLATEAU (BED_SCREWS_ADJUST)
## Pré-tensionner correctement le Kirigami
* Vissez les 3 molettes métalliques à fond jusqu'à ce que les ressorts soient complètement écrasés.
* Desserrez chaque molette de exactement 2 tours complets
## Lancer le nivellement
### Mise en chauffe
    SET_HEATER_TEMPERATURE HEATER=heater_bed TARGET=80
    SET_HEATER_TEMPERATURE HEATER=extruder TARGET=200
### Buse au centre du plateau
    G28
### Ajustement des vis du plateau
    BED_SCREWS_ADJUST

## Z-Offset
    Z_ENDSTOP_CALIBRATE
### Ajustement avec une feuille de papier
    TESTZ Z=-0.1
### Valider la valeur
    ACCEPT
### Sauvegarder la configuration (z_position_endstop)
    SAVE_CONFIG