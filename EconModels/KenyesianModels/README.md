# Keynesian Recession Simulation

## About

This project is a simple Keynesian recession model built to help me understand how recession models work and visualize the main pieces that go into them.

It is a teaching and intuition tool, not a forecasting model.

## What is a Keynesian model?

A Keynesian model assumes that economic output is driven by aggregate demand. In simpler terms the Keynesian view is that when the demand decreases the chain reaction leads to a recession. In this model taxes and tax policy are not included, but they could be added in a more complex version. This model also does not include exports which also could be added in a more complex version.

When spending falls:
- firms sell less
- output falls
- unemployment rises
- weaker income and labor markets can reduce spending further

That feedback loop is the basic Keynesian recession story.

## Model equations

### Output
\[
Y_t = C_t + I_t + G
\]

- \(Y_t\): output (gross domestic product, GDP) at time \(t\)
- \(C_t\): consumption (household spending)
- \(I_t\): investment (business spending)
- \(G\): government spending (assumed constant in this model)

### Consumption
\[
C_t = a + bY_{t-1} - cU_{t-1} + d \cdot confidence_t
\]

- \(a\): autonomous consumption (baseline consumption when income is zero)
- \(b\): marginal propensity to consume (how much consumption changes with income)
- \(Y_{t-1}\): previous output  (income from the previous period)
- \(c\): unemployment sensitivity (how much consumption changes with unemployment)
- \(U_{t-1}\): previous unemployment  (unemployment from the previous period)
- \(d \cdot confidence_t\): confidence effect on spending (how much consumption changes with consumer confidence)

### Investment
\[
I_t = i_0 - i_r r_t + i_c \cdot confidence_t
\]

- \(i_0\): baseline investment (investment when interest rates are zero and confidence is neutral)
- \(r_t\): interest rate (the cost of borrowing)
- \(i_r\): interest-rate sensitivity (how much investment changes with interest rates)
- \(i_c \cdot confidence_t\): confidence effect on investment (how much investment changes with business confidence)

### Unemployment
\[
U_t = U^* + \alpha \cdot \max(0, Y^* - Y_t)
\]

- \(U_t\): unemployment rate (current unemployment)
- \(U^*\): natural unemployment rate (the unemployment rate when the economy is at potential output)
- \(Y^*\): potential output (the level of output the economy can sustain without generating inflation)
- \(\alpha\): sensitivity to the output gap (how much unemployment changes when output is below potential)

## Recession mechanism

The model generates a recession through a negative confidence shock:

lower confidence -> lower consumption and investment -> lower output -> higher unemployment -> lower spending again

## Purpose

This project is mainly for learning:
- understanding the structure of a basic Keynesian recession model
- visualizing how macro variables interact
- seeing how a recession can develop over time

## Author
- Prashun Kafle. 