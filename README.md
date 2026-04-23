# Low Pass Filter

\[
V_{in}(t) = V_R(t) + V_C(t)
\]

\[
V_C(t) = \frac{q}{C} = V_{out}(t)
\]

\[
V_R(t) = \frac{dq}{dt} \cdot R = RC \frac{dV_{out}(t)}{dt}
\]

\[
V_{in}(t) = RC \frac{dV_{out}(t)}{dt} + V_{out}(t)
\]

## By Laplace Transform

\[
V_{in}(s) = sRC \cdot V_{out}(s) + V_{out}(s)
\]

## Transfer Function

\[
H(s) = \frac{V_{out}(s)}{V_{in}(s)} = \frac{1}{1 + sRC}
\]

## Cutoff Frequency

\[
f = \frac{1}{2\pi RC}
\]
## High Pass Filter

\[
V_{in}(t) = V_R(t) + V_C(t)
\]

\[
V_R(t) = V_{out}(t) = R \frac{dq}{dt}
\]

\[
V_C(t) = \frac{1}{RC} \int V_{out}(t)\,dt
\]

\[
V_{in}(t) = V_{out}(t) + \frac{1}{RC} \int V_{out}(t)\,dt
\]

**By Laplace Transform**
## Transfer Function

\[
H(s) = \frac{V_{out}(s)}{V_{in}(s)} = \frac{sRC}{1 + sRC}
\]

Here, frequency:
\[
f = \frac{1}{2\pi RC}
\]

---

## Band Pass Filter

It is a combination of a **High Pass Filter** and a **Low Pass Filter**,  
i.e., the output of the high-pass filter is fed as input to the low-pass filter.

---

### High Pass Filter Transfer Function

\[
H(s) = \frac{V_{out}(s)}{V_{in}(s)} = \frac{sR_1C_1}{1 + sR_1C_1}
\]

Lower cutoff frequency:
\[
f_L = \frac{1}{2\pi R_1 C_1}
\]

---

### Low Pass Filter Transfer Function

\[
H(s) = \frac{V_{out}(s)}{V_1(s)} = \frac{1}{1 + sR_2C_2}
\]

Upper cutoff frequency:
\[
f_H = \frac{1}{2\pi R_2 C_2}
\]

---

### Final Transfer Function

\[
H(s) = \frac{V_{out}(s)}{V_{in}(s)} = 
\frac{sR_1C_1}{(1 + sR_1C_1)(1 + sR_2C_2)}
\]

---

### Bandwidth

\[
\text{Bandwidth} = f_H - f_L
\]
