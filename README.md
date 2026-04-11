# Barn-Door-Tracker Webpage

## What this guide contains?

1. The theory
2. Calculator
3. The math
4. The process


## Theory

A barn door tracker (or Scotch mount) is a mechanical device used to compensate for the Earth's rotation. Using a curved bolt specifically eliminates "tangent error," allowing for longer exposures without star trailing.

### 1. Polar Alignment (The Foundation)
* **The Hinge Axis:** The two boards are joined by a hinge that must be aligned parallel to the Earth's axis. This means the hinge must point directly at the North or South Celestial Pole (e.g., Polaris in the Northern Hemisphere).
* **Rotational Compensation:** As the Earth rotates East to West at approximately **15.04° per hour**, the tracker opens the boards at the same rate in the opposite direction.

### 2. Eliminating Tangent Error
* **The Problem:** In straight-bolt designs, the rate of opening is based on a tangent function. As the angle increases, a constant motor speed results in a slowing angular velocity, causing "trails" after about 5–10 minutes.
* **The Curved Bolt Solution:** By bending the threaded rod into a circle with its center at the hinge, the distance from the hinge to the bolt ($R$) remains constant.
* **Linearity:** Because the radius is fixed, the linear movement of the nut along the bolt translates into a perfectly linear angular movement of the boards.



### 3. Single Motor Synchronization
* **Mechanism:** A single motor (usually a stepper or a DC gear motor) turns a nut or the bolt itself at a constant RPM.
* **The Math:** To achieve the sidereal rate, the distance from the hinge to the bolt ($R$) is determined by the motor speed and the thread pitch.
* **Calculation:** If $P$ is the pitch of the thread (distance per revolution) and $T$ is the time for one revolution in minutes, the radius $R$ is calculated as:
  
  $$R = \frac{P \cdot 1436.07}{2\pi \cdot T}$$

### 4. Declination and Mounting
* **RA Axis:** The motor-driven opening handles the **Right Ascension** (tracking).
* **Declination Axis:** A ball head is typically mounted on the top board. This allows the camera to "decline" or pivot to different altitudes in the sky while the entire platform rotates to follow the stars.

### 5. Summary of Benefits
* **Extended Exposures:** Curved bolts support 20+ minute exposures with wide lenses.
* **Mechanical Simplicity:** Only one moving part (the motor/bolt assembly) is required to track the sky.
* **High Precision:** Replaces expensive equatorial mounts for entry-level astrophotography.