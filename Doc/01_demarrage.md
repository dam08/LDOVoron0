# Premier demarrage
## 1 - Test du endstop Z
### Placez le plateau et l'outil au milieu de l'imprimante, à la main (machine éteinte).
    QUERY_ENDSTOPS

*Klipper doit vous répondre que Z est en etat open.*
### Appuyez avec votre doigt sur le switch Z (en bas de l'imprimante) et maintenez-le enfoncé.
    QUERY_ENDSTOPS
*L'axe Z doit maintenant être sur l'etat TRIGGERED.*

## 2 - Test du endstop X, Y
    G28 X
    G28 Y

## 3 - Le sens de rotation des moteurs
*Vérifier que les moteurs tournent dans le bon sens sans faire de Home complet*
### Axe Z
Dans l'interface, cliquez sur la flèche pour faire descendre le plateau de 1 ou 5 mm (Z+).

*Le plateau doit physiquement descendre. S'il monte, éteignez tout. Vous devrez ajouter un point d'exclamation ! devant la broche dir_pin de votre [stepper_z] dans Klipper pour inverser le sens.*
### Axes X/Y
    FORCE_MOVE STEPPER=stepper_x DISTANCE=10 VELOCITY=20
    FORCE_MOVE STEPPER=stepper_y DISTANCE=10 VELOCITY=20

## 4 - Premiers tests de chauffe
    SET_HEATER_TEMPERATURE HEATER=heater_bed TARGET=40
    SET_HEATER_TEMPERATURE HEATER=extruder TARGET=150