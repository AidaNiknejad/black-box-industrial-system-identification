# Black-Box Identification of a High-Order Time-Delay System

A system identification project focused on modeling a high-order industrial process with time delay under limited black-box access.

The project uses step-response identification, relay-feedback testing, PRBS excitation, and least-squares estimation to obtain continuous and discrete models of the unknown process.

## Project Overview

In many industrial applications, the internal structure and physical parameters of a process are not completely available.

Under these conditions, the process can be treated as a black-box system and modeled using measured input-output data.

In this project, a high-order system with time delay was implemented in Simulink. Band-limited white noise was added to represent measurement and process disturbances.

Three identification approaches were then applied:

1. Two-point step-response identification
2. Relay-feedback analysis
3. PRBS-based discrete ARX identification

## Project Objectives

- Simulate a high-order industrial process with time delay
- Add band-limited white noise to the simulated process
- Analyze the step response of the unknown system
- Identify an FOPDT model using the two-point method
- Perform relay-feedback testing
- Determine critical frequency-domain parameters
- Generate a PRBS input signal
- Estimate a discrete ARX model using least squares
- Compare identified models with the original process
- Evaluate model accuracy and dynamic similarity

## Black-Box Identification

Black-box identification develops a mathematical model using only measured input and output signals.

The internal equations and physical parameters of the process are assumed to be unavailable.

The general identification workflow includes:

1. Applying a suitable excitation signal
2. Recording the process output
3. Preprocessing the measured data
4. Selecting a model structure
5. Estimating model parameters
6. Validating the identified model
7. Comparing the model with the original process

## Original Process

The studied process is characterized by:

- High-order dynamics
- Time delay
- Limited internal information
- Band-limited white noise
- Industrial process behavior
- Continuous- and discrete-time representations

The original system was implemented in the Simulink environment.

## FOPDT Identification

A First-Order Plus Dead-Time model was extracted from the process step response using the two-point method.

The identified model has the general form:

```text
             K
G(s) = ------------- e^(-Ls)
           Ts + 1
