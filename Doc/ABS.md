# ABS
## Part Cooling Fan (OrcaSlicer:  Filament -> Refroidissement)
1) Activer le refroidissement du filament : Coché (Oui)
2) Vitesse minimale du ventilateur : 15% à 20% (C'est la vitesse constante pour maintenir la cloche de l'enceinte homogène sans refroidir brutalement la pièce)
3) Vitesse maximale du ventilateur : 40% à 50%. (Sera activée uniquement sur les couches très courtes, inférieures à 5-10 secondes, comme les petites pointes ou fins de pièces).
4) Désactiver le ventilateur pour les [ 3 ] premières couches : L'ABS a besoin d'une absence totale d'air au départ pour fusionner parfaitement avec le plateau (PEI).
5) Vitesse du ventilateur pour les ponts (Overhang/Bridge fan speed) : 60% à 80%. Pour réussir un pont dans le vide, l'ABS a besoin d'être figé instantanément, sinon il coule et crée des fils massifs.
## Hotend Fan (Klipper)
### 01_skr_pico.cfg
    [heater_fan hotend_fan]
    pin: gpio18
    max_power: 1.0
    kick_start_time: 0.5
    heater: extruder
    heater_temp: 50.0
    fan_speed: 1.0