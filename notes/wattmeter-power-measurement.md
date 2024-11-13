---
title: 'Wattmeter Power Measurement Method in three phase AC systems.'
description: 'General formulas + ideas.'
tags: ['wattmeter', 'ac', 'power', 'measurement']
---

# Wattmeter Power Measurement Method

## Star connected load using 2 Wattmeters

![Two Wattmeter Method of Power Measurement - ElectricalWorkbook](https://electricalworkbook.com/wp-content/uploads/2021/07/Two-Wattmeter-Method-of-Power-Measurement-1024x799.png)

- W<sub>1</sub> + W<sub>2</sub> = <span style="color:red">**Total Active Power**</span>

- $W_1 + W_2 = \sqrt3 \times V_L \times I_L \times \cos\theta$

- $W_2 - W_1 = V_L \times I_L \times \sin\theta$

- $\frac{W_2-W_1}{W_2+W_1} = \frac{\sin\theta}{\sqrt3\cos\theta}$

- $\theta = \tan^{-1}[\sqrt3\times\frac{W_2 - W_1}{W_2 + W_1}]$

- Core Idea:
  
  - **Connection**: The two wattmeters are connected so that each one measures the power in a different phase. The current coils of the wattmeters are connected in series with two of the line conductors (phases), and the voltage coils are connected between these conductors and the third phase.
  
  - **Voltage Reference**: Each wattmeter has its voltage coil connected between its respective line and the third line, making the angle between the current and voltage for each wattmeter different.
  
  - The method works on the principle that in a balanced or unbalanced three-phase, three-wire system, the sum of the power measured by the two wattmeters equals the total power consumed.
  
  - This approach allows for the measurement of power even when the system is unbalanced, unlike the single wattmeter method.
