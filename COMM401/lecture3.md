# Properties of Systems

## Linearity
- Input $x_1(t)$ to the system to get $y_1(t)$
- Input $x_2(t)$ to the system to get $y_2(t)$
- Input $x_3(t)$ to the system to get $y_3(t)$ where $x_3(t) = ax_1(t) + bx_2(t)$
- If $y_3(t) = ay_1(t) + by_2(t)$ then the system is linear!
- Otherwise, the system is non-linear.

## Time Invariance
- Input $x_1(t)$ to the system to get $y_1(t)$
- Input $x_2(t)$ to the system to get $y_2(t)$ where $x_2(t) = x_1(t-t_0)$
- If $y_2(t) = y_1(t-t_0)$ then the system is time invariant.
- Otherwise, it's time variant. *(NOT time invariant)*

## Memory
A system is memoryless if the output at any time depends only on the input at the same time.

## Causality
A system is causal if the output doesn't depend on the future. *(Only depends on past and present values)*

> All memoryless systems are causal.

## Stability
A system is stable if we input a bounded input and the output is also bounded.
- We claim the input $x(t)$ is bounded.
- We try to get a maximum for the output $y(t)$
- If $max\{y(t)\}$ is finite $\rightarrow$ System is stable.
- If $max\{y(t)\}$ is infinite $\rightarrow$ System is NOT stable.

## Invertibility
A system is invertible if a distinct input leads to a distinct output.
> We can get an inverse to an invertible system.

- We try different inputs to try and get the same output. Sometimes variants of dirac help.

# Linear Time-Invarient Systems

- LTI systems can be easily studied in detail.
- They're characterized by their unit impluse response $h(t)$ which is the output when input is $\delta(t)$.

$$ y[n] = \sum_{k=-\infty}^{\infty} x[k]h[n-k] $$

The above sum is called the convolution sum and is denoted by the symbol $*$

## Conditions

| Property      | Rule                                         |
| ------------- | -------------------------------------------- |
| Memoryless        | $h(t) = k\delta(t)$                          |
| Invertibility | $h(t) * h_{inv}(t) = \delta(t)$              |
| Causality     | $h(t) = 0$ for $t < 0$                       |
| Stability     | $\int_{-\infty}^\infty \|h(t)\| dt < \infty$ |