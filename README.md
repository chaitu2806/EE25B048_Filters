## Low Pass Filter

$$
V_{in}(t) = V_R(t) + V_C(t)
$$

$$
V_C(t) = \frac{q}{C} = V_{out}(t)
$$

$$
V_R(t) = R \frac{dq}{dt} = RC \frac{dV_{out}(t)}{dt}
$$

$$
V_{in}(t) = RC \frac{dV_{out}(t)}{dt} + V_{out}(t)
$$

### By Laplace Transform

$$
V_{in}(s) = RC \cdot s \, V_{out}(s) + V_{out}(s)
$$

$$
V_{in}(s) = V_{out}(s)(1 + sRC)
$$

$$
H(s) = \frac{V_{out}(s)}{V_{in}(s)} = \frac{1}{1 + sRC}
$$

Cutoff Frequency:
$f_c = \frac{1}{2\pi RC}$

---

## High Pass Filter

$$
V_{in}(t) = V_R(t) + V_C(t)
$$

$$
V_R(t) = V_{out}(t) = R \frac{dq}{dt}
$$

$$
V_C(t) = \frac{1}{RC} \int V_{out}(t)\, dt
$$

$$
V_{in}(t) = V_{out}(t) + \frac{1}{RC} \int V_{out}(t)\, dt
$$

### By Laplace Transform

$$
V_{in}(s) = V_{out}(s) + \frac{1}{RC} \cdot \frac{1}{s} V_{out}(s)
$$

$$
V_{in}(s) = V_{out}(s)\left(1 + \frac{1}{sRC}\right)
$$

$$
H(s) = \frac{V_{out}(s)}{V_{in}(s)} = \frac{sRC}{1 + sRC}
$$

Cutoff Frequency:
$f_c = \frac{1}{2\pi RC}$

---

## Band Pass Filter

It is a combination of a *High Pass Filter* followed by a *Low Pass Filter*.

---

### High Pass Stage

$$
H_{HP}(s) = \frac{sR_1C_1}{1 + sR_1C_1}
$$

$$
f_L = \frac{1}{2\pi R_1 C_1}
$$

---

### Low Pass Stage

$$
H_{LP}(s) = \frac{1}{1 + sR_2C_2}
$$

$$
f_H = \frac{1}{2\pi R_2 C_2}
$$

---

### Overall Band Pass Transfer Function

$$
H(s) = \frac{sR_1C_1}{(1 + sR_1C_1)(1 + sR_2C_2)}
$$

Bandwidth:
$\text{BW} = f_H - f_L$
