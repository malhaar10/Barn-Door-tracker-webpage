# Barn-Door-Tracker Webpage

A barn door tracker (or Scotch mount) is a mechanical device used to compensate for the Earth's rotation. Using a curved bolt specifically eliminates "tangent error," allowing for longer exposures without star trailing.

## What this guide contains?

1. The theory
2. Calculator
3. The math
4. The process


### Theory
The curved-bolt barn door tracker is a mechanical analog device designed to neutralize the Earth's apparent rotation for long-exposure astrophotography.

1. Polar Alignment (The Foundation)
* **The Hinge Axis:** The two boards are joined by a hinge that must be aligned parallel to the Earth's axis. This means the hinge must point directly at the North or South Celestial Pole (e.g., Polaris in the Northern Hemisphere).
* **Rotational Compensation:** As the Earth rotates East to West at approximately **15.04° per hour**, the tracker opens the boards at the same rate in the opposite direction.

2. Eliminating Tangent Error
* **The Problem:** In straight-bolt designs, the rate of opening is based on a tangent function. As the angle increases, a constant motor speed results in a slowing angular velocity, causing "trails" after about 5–10 minutes.
* **The Curved Bolt Solution:** By bending the threaded rod into a circle with its center at the hinge, the distance from the hinge to the bolt ($R$) remains constant.
* **Linearity:** Because the radius is fixed, the linear movement of the nut along the bolt translates into a perfectly linear angular movement of the boards.



3. Single Motor Synchronization
* **Mechanism:** A single motor (usually a stepper or a DC gear motor) turns a nut or the bolt itself at a constant RPM.
* **The Math:** To achieve the sidereal rate, the distance from the hinge to the bolt ($R$) is determined by the motor speed and the thread pitch.
* **Calculation:** If $P$ is the pitch of the thread (distance per revolution) and $T$ is the time for one revolution in minutes, the radius $R$ is calculated as:
  
  $$R = \frac{P \cdot 1436.07}{2\pi \cdot T}$$

4. Declination and Mounting
* **RA Axis:** The motor-driven opening handles the **Right Ascension** (tracking).
* **Declination Axis:** A ball head is typically mounted on the top board. This allows the camera to "decline" or pivot to different altitudes in the sky while the entire platform rotates to follow the stars.



---

### Calculator
*(Section intentionally left blank)*

---

### Math
To synchronize the tracker with the stars, the physical dimensions must match the Earth's sidereal rotation rate.

* **The Sidereal Rate ($\omega$):**
    The Earth rotates $360^{\circ}$ in one sidereal day ($1,436.07$ minutes).
    $$\omega = \frac{2\pi}{1436.07} \approx 0.004375 \text{ radians/min}$$

* **The Drive Radius ($R$):**
    This is the distance from the center of the hinge pin to the center of the curved bolt. To find $R$, we equate the linear speed of the nut on the bolt to the required tangential speed at that radius.
    $$R = \frac{P \cdot RPM}{\omega}$$
    Where:
    * **$R$**: Distance from hinge to bolt (mm or inches).
    * **$P$**: Pitch of the thread (distance moved per full revolution, e.g., $1/20$ inch for a 1/4-20 bolt).
    * **$RPM$**: Revolutions per minute of the motor.

* **Bolt Curvature:**
    The bolt must be bent to a radius exactly equal to $R$. If the bolt is bent to a different radius than the distance it is mounted from the hinge, the mechanism will bind or introduce tracking inaccuracies.

* **Tracking Error (Simplified):**
    While the curved bolt removes geometric tangent error, the remaining error $E$ is typically a function of polar misalignment:
    $$E \approx \Delta\theta \cdot \sin(\delta)$$
    *(Where $\Delta\theta$ is the alignment error and $\delta$ is the declination of the target object).*


