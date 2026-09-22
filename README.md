# Parker Solar Probe Venus flyby in GMAT
A flyby (or gravity assist) is a technique used to reduce or increase the relative velocity to a central body, in our case to the Sun. This technique was used in multiple mission, for example the Parker Solar Probe, which used seven flyby of Venus, to lower its perihelion to study closer the Sun.
It use the gravity of the planet that, depending if it happens in front or behind the planetary motion, rotate the velocity vector.
Mathematically if $\vec{v_P}$ is the velocity of the planet's orbit around the Sun and $\vec{v_S}$ is the velocity of the spacecraft inside the planet's sphere of influence(SOI), therefore the absolute velocity relative to the Sun at any istant is given by:

$$
\vec{v} = \vec{v_P} + \vec{v_S}
$$

For the analysis of this maneuver, knowledge of the method of the patched conics is required, since at every moment of trajectory we must decide a primary body which define the gravitation attraction.
The radius of the SOI of Venus can be calculated by the formula:

$$
R_{SV} = a_{Venus} (\frac{m_V}{m_S})^{\frac{2}{5}} \approx 616,740 km
$$

Using NASA's data, we find that the entrance in the SOI of Venus for the first flyby happened on October, 3, 2018 at 01:20 a.m. (UTC Gregorian), and cartesian coordinate respect to a ICRF frame centered in Venus:


$x = 568,496.1905081868$ $km$

$y = 233,432.7319901772$ $km$

$z = 36,315.33797430247$ $km$

$v_x = -21.29376455341736$ $\frac{km}{s}$

$v_y = -8.437572269229019$ $\frac{km}{s}$

$v_z = -1.53968891276164$ $\frac{km}{s}$


Converting these data into the keplerian parameters of the hyperbolic trajectory gives:

$\epsilon = 262.97$ $\frac{km^2}{s^2}$ $h = 208,494.6$  $\frac{km^2}{s}$ $i = 33.46^\circ$ $e = 14.75$ $\Omega = 207.5^\circ$ $\theta = -93.04^\circ$

Using the relations bewteen angles and times for the hyperbolic orbit we find an approximated value of time till the PSP exit the SOI of Venus of $\Delta t = 53,412$ $s$.
We input these data in GMAT simulating the orbit and plotting the graph of the velocity of the PSP along all the orbit relative to an ICRF frame centered in the Sun.

<img width="849" height="372" alt="image" src="https://github.com/user-attachments/assets/783ddf19-d3ca-4977-a079-48e51242bce0" />

Radiaton solar pressure was ignored in this analysis.

## Conclusion

As we can see in the graph the spacecraft, passed in front of the planet's orbit, resulting in a loss of orbital energy respect to the Sun, which lowers the perihelion, making this maneuver a success.
