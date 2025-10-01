<<<<<<< HEAD
\# Solar Car Simulation

This repository contains a simple modular simulation of a solar car.

The strategy and assumptions used in this approach:
•Discretize distance into smaller parts with constant properties that can be used as a state.
•Road is assumed to be a straight line throughout without any elevation.

Parameters that play important role in this strategy:
•Irradiation from sun during active hours (8am-5pm) changes and should be incorporated in the calculations.
•Effects from winds. (assume crosswinds to affect only direction of motion, no toppling considered)


IRRADIANCE:
Length of race = 3000km = 3000000m
Time taken (iteration method) = 5 days (x9hrs/day)
Average velocity of car = 66.6kmph
Discretized states = Every 100km or 1.5 hrs during active time
Staring point: 24 August 8am
Ending point: 30 August 5pm


•Using data from excel provided, we need to average step distance to 100km and all other rows of 20 values into 1. Using averaged latitude, longitude and approximating values of hour angle, solar zenith angle and air mass, we can find Direct Normal Irradiance (DNI) and Global Horizontal Irradiance (GHI) and table the values.
•Assume solar panel Area = 6m^2, solar panel efficiency = 23%, electronics efficiency = 95%
•We can find Power usable by multiplying the solar irradiance by a factor 1.3.


Effects from winds:
•Assume a constant wind speed of 40kmph and the direction variation is averaged for 20 rows into 1, Projected normal surface area of car to be 2m^2, coefficient of drag = 0.18, air density = 1.1752.
•Using the formula for drag --- we can table the values of this drag force.
•We can calculate the average power required to overcome this drag force which is approximately 350W.
Conclusion:
•For the current case, the power required from battery is approx. 1500W which can last for 3-5hrs which is not optimal to finish the race.
•Reducing the average velocity to 50kmph reduces the power required form battery to <500W which is more than sufficient to finish the race. 
•Hence, we can say that the average velocity lies between 50-66.6kmph.
•Considering the irradiance behaviour throughout the active hours, which achieves a peak value near noon, I can imagine the velocity profile to start slow and reach a max value at noon/past noon and then slowly decrease and reach a point above initial velocity almost resembling the irradiance profile.


=======
# solar-car-simulation
>>>>>>> a453b94fe03d4e172cd255a9943d1ebce410f808
