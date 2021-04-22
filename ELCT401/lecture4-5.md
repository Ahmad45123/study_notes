# Power Calculation

## Instantaneous Power
It's the product of the instant voltage and current. The positive sign is used when the reference direction for the current is from positive to negative voltage.

$$ p = vi $$

> - Frequency of instant power is twice the frequency of the voltage or current.
> - Instant power may be negative for a portion of each cycle 

## Average Power
It's the average of the instantaneous power over one period. It's the power converted from electric to nonelectric forms or vice versa.
It's also called **real power**.

$$ P = \frac{1}{2} V_m I_m cos(\theta_v - \theta_i) = V_{eff} I_{eff} cos(\theta_v - \theta_i)$$

## Reactive Power
It's the power exchanged between the magnetic field of an inductor and the source or the electric field of a capacitor and the source. Reactive power is NEVER converted to nonelectric power.

$$ Q = \frac{1}{2} V_m I_m sin(\theta_v - \theta_i) = V_{eff} I_{eff} sin(\theta_v - \theta_i)$$

> *Effective value* and *rms value* are interchangeable terms for the same value.

## Power Factor
$$ pf = cos(\theta_v - \theta_i) $$

- If it's **lagging**, then the current is lagging the voltage and the circuit is **inductive**!
- If it's **leading**, then the current is leading the voltage and the circuit is **capacitive**.


## Reactive Factor
$$ rf = sin(\theta_v - \theta_i) $$

## Complex Power
It's the complex sum of the real and reactive powers.

$$ S = P + jQ $$
$$ S = \frac{1}{2} V I^* = V_{eff} I_{eff}^* $$
$$ S = I_{eff}^2 Z = \frac{V_{eff}^2}{Z^*} $$

## Apparent Power 
It's the magnitude of the complex power: 

$$ |S| = \sqrt{P^2 + Q^2} $$

> **Watt** is the unit for real power while **VAR** is the unit for reactive power. **VA** is the unit for apparent power.

# Power Factor Correction
It is the process of increasing the power factor without altering the voltage or current to the original load. It's done by connecting a parallel capacitor to the circuit to compensate.

$$ C = \frac{Q_C}{\omega V_{rms}^2} = \frac{P (tan\theta_1 - tan\theta_2)}{\omega V_{rms}^2}$$

# Maximum Power Transfer
Occurs when the load is the conjugate of the Thevenin Impedance. $Z_L = Z_{th}^*$

$$ P_{max} = \frac{1}{4} \frac{|V_{th}|^2}{R_L} = \frac{1}{8} \frac{V_m^2}{R_L}$$