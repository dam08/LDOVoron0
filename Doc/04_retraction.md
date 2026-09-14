# Retraction
## OrcaSlicer
1) Edition de l'imprimante
2) Onglet Extruder
3) Cochez la case Rétraction par le firmware (Use firmware retraction)
## Rappel des parametres dans 05_settings.cfg
    [firmware_retraction]
    retract_length: 0.5
    retract_speed: 35
    unretract_extra_length: 0
    unretract_speed: 30
## Modifier en cours d'impression 
    SET_RETRACTION RETRACT_LENGTH=0.6