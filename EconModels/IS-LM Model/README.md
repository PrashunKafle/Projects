# Simple IS-LM Model

## Overview

This project is a basic IS-LM macroeconomic model built to help me understand how output and interest rates are determined by the interaction between the goods market and the money market.

It is a learning model for visualizing how a demand shock can push the economy into a recession.

## What the model does

The model plots:
- the IS curve
- the LM curve
- a shifted IS curve after a negative demand shock

It then finds the equilibrium before and after the shock.

This makes it easier to see how lower demand leads to:
- lower output
- lower interest rates

## What is the IS-LM model?

The IS-LM model is a simple macroeconomic framework that combines:

- the **IS curve**, which represents equilibrium in the goods market
- the **LM curve**, which represents equilibrium in the money market

The point where they intersect gives the economy’s equilibrium:
- output
- interest rate

## Model equations

### IS curve

\[
Y = a + bY - cr
\]

This is the goods market equation.

- \(Y\): output
- \(a\): autonomous demand
- \(b\): marginal propensity to spend
- \(c\): sensitivity of investment to interest rates
- \(r\): interest rate

Rearranged into graph form:

\[
r = \frac{a - (1-b)Y}{c}
\]

What it means:
- higher interest rates reduce investment
- lower investment reduces total demand
- so the IS curve slopes downward

### LM curve

\[
\frac{M}{P} = kY - hr
\]

This is the money market equation.

- \(M/P\): real money supply
- \(k\): how strongly money demand rises with income
- \(h\): how strongly money demand responds to interest rates
- \(Y\): output
- \(r\): interest rate

Rearranged into graph form:

\[
r = \frac{kY - M/P}{h}
\]

What it means:
- higher income increases money demand
- with a fixed money supply, higher money demand pushes interest rates up
- so the LM curve slopes upward

## Negative demand shock

The model simulates a recession by lowering autonomous demand:

\[
a_{shock} < a
\]

This shifts the IS curve left.

What happens after the shock:
- demand falls
- output falls
- interest rates fall
- the economy moves to a lower equilibrium

## How the code works

The code:
- defines parameter values for the IS and LM equations
- creates a range of output values
- calculates the IS and LM interest rates for each output level
- creates a second IS curve with lower demand
- finds where the curves intersect
- plots the original equilibrium and the recession equilibrium

## Purpose

This project is mainly for me to understand the structure of the IS-LM model and visualize how a simple demand shock affects output and interest rates.

## Author
Prashun Kafle.