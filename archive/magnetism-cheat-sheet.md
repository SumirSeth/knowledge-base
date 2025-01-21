---
title: "Cheat sheet for Magnetism"
description: "Cheat sheet for Magnetism for my first year engineering course."
tags: ['magnetism', 'forumals', 'electronics']
---

# Magnetism Cheat Sheet

## 4.1 Basics of Magnetism

### Properties of Magnetic Lines

ML of Force is an imaginary line representing the direction of magnetic field such that the tangent at any point is the direction of the field vector at that point.

- Magnetic line form a closed path.

- Magnetic line are like strecthed elastic cord always trying to shorten themselves.

- Magnetic line which are parallel in the same direction repel each other.

---

### Magnetic Flux

- Symbol : $\phi$

- Total number of magnetic <u>field lines penetrating any surface placed perpendicular </u>to the magnetic field.

- $\phi = \int B.ds$

- Unit : Weber (Wb)

- <span style="color:yellow">Analogous to :</span> Electric Current

### Magnetic Flux Density

- Symbol = $B$

- Magnetic flux per unit area. <u>Density measured in context of area</u>.

- $B = \phi /A$

- Unit : Wb/m^2 (<u>Tesla</u>)

- <span style="color:yellow">Analogous to :</span> Current Density

### Magneto Motive Force

- Symbol : F

- <u>Force which drives the magnetic lines of force</u> through a magnetic circuit.

- $F = \phi \times S$
  $F = N \times I$

- Unit : AT (Ampere Turns)

- <span style="color:yellow">Analogous to :</span> EMF

### Magnetic Field Strength

- Symbol : H

- => Magnetic Field Strength. <u>Magneto motive force per unit length</u>.

- $H = (N \times I) / l$

- Unit : AT/m

- <span style="color:yellow">Analogous to :</span> Electric Field Strength

### Permeability

- Symbol : $\mu$

- Property of a material indicative of its ability to carry magnetic flux. Or, <u>a property of materials that measures how easily a magnetic field can pass through them</u>.

- $\mu = B / H$

- Unit : H/m

- Relative permeability : $\mu_r = \mu/\mu_0$ 

- <span style="color:yellow">Analogous to :</span> Conductivity

### Reluctance

- Symbol : S

- The measure of <u>opposition</u> the magnetic circuit offers to the flux.

- $S = \frac{l}{\mu_0\mu_rA}$

- <span style="color:yellow">Analogous to :</span> Resistance

---

### Direction of Mag Field

Use the right hand rule.

### Mag Field in a Solenoid

A coil of wire that acts as a magnet when an electric current flows through it.

$B = \frac{\mu_0NI}{l}$

![Solenoid Magnetic Field Gcse at Christine Davis blog](https://www.sciencefacts.net/wp-content/uploads/2021/09/Solenoid-Magnetic-Field-Equation.jpg)

where n = N/l, n = turns per unit length

### Classification of Materials

- Linear 
  
  - Diamagnetic
  
  - Para

- Non Linear
  
  - Ferro

---

### Losses in Magnetic Circuit

- <u>**Hysteresis loss**</u> is caused due to *molecular friction* in a ferromagnetic material, under alternating magnetic field.
  
  - The energy dissipated as *heat* in the process of magnetisation and de-magnetisation.
  
  - This heat loss is proportional to the hysterisis loop area (obviously).

- <u>**Eddy Current Loss**</u> is the loss which is caused due to the induced current within a material. (In accordance to Faraday's Law of Induction)

---

### Major difference between Electric and Magnetic Circuit Analogies

- Current Actually flows. Magnetic flux does not *flow* in that sense.

- Current can NOT flow in air / vacuum. Flux *can* be created in air / vacuum.

---

## 4.2 Series Magnetic Circuits

### Magnetic Circuits

- The complete closed path followed by magnetic lines of flux is called magnetic circuit.

- ![PPT - Chapter 1 MAGNETIC CIRCUIT PowerPoint Presentation, free download ...](https://image2.slideserve.com/3805831/slide6-l.jpg)

### Series Mag Circuit

- Flux is same if linkage flux is neglected.

- Magnetic flux density and reluctance in each section may vary.

- The resultant MMF is the **sum of MMF of each part**.

- Equivalent Reluctance is just simply the **sum of reluc of each part**.

- S<sub>total</sub> = S<sub>1</sub> + S<sub>2</sub> . . . + S<sub>g</sub>

### Useful and Leakage Flux

- When the flux does not follow it's intended path, its termed as leakage flux.

- This flux is NOT used for **any useful work**.

- Denoted by : $\phi_L$

- Flux utilised by the ciruict is : useful flux

- Denoted by : $\phi_u$

- Total flux: $\phi = \phi_L + \phi_u$

- **<u>Leakage Coefficient</u>** : 
  
  - $\lambda = \frac{total\space flux\space of\space coil}{Useful \space flux}$

## 4.3 Parallel Magnetic Circuit

- **When flux has <u>more than one closed path to choose from</u>**.

- > More notes to be added here.

## 4.4 Electromagnetic Induction

### Faraday's Laws of EMI

1. First Law:
   
   - When a conductor cuts or it is cut by magnetic flux, an emf is induced in the conductor.

2. Second Law:
   
   - The magnitude of the induced emf is proportional to the tate at which the conductor cuts or is cut by the magnetic flux.
   
   - $e = N\frac{d\phi}{dt}$

### Lenz's Law

The EMF always acts in such a direction to opose to causation of the induction.

### Types of Induced EMF

- Dynamically induced EMF
  
  - The voltage induced in the conductor due to relative motion of conductor and magnetic field.
  
  - $e = blv \sin\theta$
  
  - Either conductor or magnetic field is moving
  
  - **Principle of Electric Generator**

- Statically Induced EMF
  
  - The voltage induced in the conductor due to change in the magnetic field
  
  - **Conductor is <u>stationary</u>**.
  
  - Eg - **Transformer**

### Types of Statically induced EMF

- <u>**Self Induced EMF**</u>
  
  - $e = -L\frac{di}{dt}$

- <u>**Self Inductance L**</u>:
  
  - $L = N\frac{d\phi}{di}$

- **<u>Mutually Induced EMF</u>**
  
  - The infuced emf in a coil due to change of the flux produced by the change of current in the nearby coil.

- <u>**Mutual Inductance**</u> (M)
  
  - This proportionality constant is called the mutual inductance, M.
  
  - **If coil 1 is excited** :
    
    - Mutually induced emf e<sub>2</sub> in coil 2,
    
    - $e_2 = N_2\frac{d\phi_{12}}{dt} = M\frac{di_1}{dt}$
    
    - $M = N_2\frac{d\phi_{12}}{di_1}$ 
  
  - **If coil 2 is excited** :
    
    - $M = M_2\frac{d\phi_{21}}{di_2}$

## 4.4.1 Coupled Circuits

> to be done.
