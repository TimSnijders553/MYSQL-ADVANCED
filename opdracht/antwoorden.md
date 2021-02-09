# Antwoorden Eindopdracht

1. SELECT circuits.name AS circuit, races.name AS race, races.year
FROM circuits
LEFT JOIN races ON circuits.circuitId = races.circuitId
WHERE races.year = 2018

2. Copy paste je gemaakte SQL query hieronder
   SELECT races.name AS race, races.year, driver_standing.points, drivers.surname
FROM races
INNER JOIN driver_standing ON races.raceId = driver_standing.raceId
INNER JOIN drivers ON driver_standing.driverId = drivers.driverId
WHERE races.year = 2017 AND driver_standing.points = 10
ORDER BY races.name
3. Copy paste je gemaakte SQL query hieronder
   SELECT drivers.forename, drivers.surname, pitstops.duration, pitstops.milliseconds
FROM drivers
INNER JOIN pitstops ON pitstops.driverId = drivers.driverId
WHERE pitstops.milliseconds < 25000  
4. Copy paste je gemaakte SQL query hieronder
   SELECT constructors.name, races.name, races.year
FROM constructors
INNER JOIN constructor_standing ON constructor_standing.constructorId = constructors.constructorId
INNER JOIN races ON races.raceId = constructor_standing.raceId
WHERE constructors.constructorRef = "mclaren" AND races.year = 2018
5. Copy paste je gemaakte SQL query hieronder
   SELECT circuits.name, circuits.country, races.name, drivers.surname
FROM circuits
INNER JOIN races ON races.raceId = circuits.circuitId
INNER JOIN driver_standing ON driver_standing.raceId = races.raceId
INNER JOIN drivers ON drivers.driverId = driver_standing.driverId
WHERE drivers.surname LIKE "F%" AND races.year = 1950
