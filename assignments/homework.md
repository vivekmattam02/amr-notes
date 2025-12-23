---
layout: default
title: Homework Assignments
parent: Assignments
nav_order: 1
---

# Homework Assignments
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Homework 1: Model Selection

**Objective:** Pick a robot/vehicle model that you will use throughout the course.

---

## Homework 2: Kinematics Simulation

**Objective:** Simulate the kinematics of your chosen model.

---

## Homework 3: Nonlinear Control Methods

### Requirements

1. **Plot phase portraits** of your system's error dynamics: $e$ (error) vs. $\dot{e}$ (error rate)

2. **Choose ONE approach:**
   - Robust Sliding Mode Controller **OR** 
   - Adaptive Controller
   
   Derive the Feedback Linearizable Model for your specific vehicle model.

3. **Simulate** both the controller and your vehicle model. Test with uncertainties and disturbances.

   Include simulation of:
   
   $$V_r = \frac{z^T p_b}{|z^T p_b|} \rho(x)$$

### For Sliding Mode Control

Ensure the sliding condition:

$$s \dot{s} < -\eta|s|, \quad \eta > 0$$

The control should guarantee reachability and sliding.

### For Adaptive Control

Implement parameter update law:

$$\hat{p} = \delta x^T S I_y^{-1}$$

$$\hat{P}(t) = \hat{p}(0) + \delta \int_0^t x^T S_b I_y^{-1} dt$$

---

## Homework 4: CBF Pedestrian Avoidance

**Objective:** Apply Control Barrier Functions to ensure safe robot navigation around a pedestrian.

### Requirements

1. **Scenario:** Robot must reach goal while avoiding pedestrian obstacle

2. **Define geometric constraint:**
   
   $$h(x) = \|x_{\text{robot}} - x_{\text{pedestrian}}\| - d_{\text{safe}} \geq 0$$

3. **Apply CBF approach:** Use Control Barrier Function to guarantee safety

4. **Write 5 equations:**
   - System dynamics
   - Barrier function
   - CBF condition
   - Control bounds
   - Distance formula

5. **Show solution:** Demonstrate robot reaches goal while maintaining safe distance from pedestrian

---

## Homework 5: Potential Fields

**Objective:** Implement potential fields showing two scenarios.

### Requirements

Demonstrate:

1. **Success case:** Robot successfully navigates from A to B
2. **Failure case:** Robot gets trapped in local minimum

Show both scenarios with visualizations.
