# Welcome to my Numerical Analysis Project About PCR! 🧬



# Introduction
## What is PCR? 
PCR stands for **Polymerase Chain Reaction**. It's a technique used to make copies of a small piece of DNA many times over. This helps scientists study the DNA's size and the order of its building blocks (nucleotides). PCR is like making many copies of a specific page in a book so you can study it closely and understand it better 📚

<img width="617" alt="Screenshot 2024-05-08 at 7 23 35 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/d6fc1b43-9380-41ff-ae45-f858373ecc8b">

 >> This is done using short single-stranded DNA sequences called **primers** (usually about 20 nucleotides in length), which help identify the section to be copied (**target sequence**).
During PCR, these primers bind to the DNA, and a special enzyme called **DNA polymerase** helps catalyzing the synthesis of new DNA strands by adding nucleotides to the growing DNA chain.

![image](https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/8f23aebc-e061-4ebc-92c6-e4127cb66f86)

## 3 STEPS of PCR Reaction: 
### - Denaturation
### - Annealing
### - Extension 

<img width="700" alt="image" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/9c05e61c-633e-4e71-8574-74ebfcf6d81c">

## Denaturation at 94 C
>> The double-stranded DNA molecule is heated to a high temperature, typically around 94-98°C. This high temperature causes the hydrogen bonds between the two strands of the DNA molecule to break, essentially "melting" the double helix structure and separating the two strands from each other. This separation is crucial for PCR because it exposes the individual strands of DNA, allowing the primers (short DNA sequences) to bind to their complementary sequences on each strand during the subsequent annealing step of PCR.

<img width="646" alt="image" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/a626b050-e4de-4c95-a6cd-2358d233539e">

## Annealing at 54 C
>> This is when the primers start making copies of the DNA. Primers will try to bond with the template: once the primer is firmly attached to the template, a special enzyme called DNA polymerase joins in. It starts copying the DNA, making a new strand using the template as a guide. As the copying continues, the bond between the primer and the template becomes stronger. This strong bond means the primer stays firmly attached to the template, allowing the DNA polymerase to keep copying the DNA accurately.

<img width="646" alt="image" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/92744f21-a665-4424-b5ac-7ad7ab649192">

## Extension at 72 C
>> In this phase, the primers that have successfully attached to the template DNA and have a few bases built in maintain a strong attraction to the template. This means they stay firmly bound to the template, allowing the DNA polymerase to extend the DNA strand by adding complementary bases.
However, if a primer is in a position where there's no exact match on the template, it doesn't stay bound tightly, and it can detach. In such cases, no extension of the DNA fragment occurs because there's no proper template for the DNA polymerase to copy.
The DNA polymerase adds new bases to the primer on its 3' end, following the template's sequence. This ensures that the new DNA strand is complementary to the template strand, resulting in accurate DNA replication.

<img width="608" alt="image" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/9815ded3-a592-4059-850a-e3033326e36d">

### Exponential Increase of Number of Copies
PCR copies both strands of the DNA, and each cycle of PCR doubles the amount of DNA. This means that with each cycle, the number of DNA copies increases exponentially. So, if you start with just a few copies of a gene, after a few cycles of PCR, you'll have a lot more copies. 

### 30 cycles of PCR >> 1.07 billion times more DNA
### 40 cycles of PCR >> 1.1 trillion times more DNA

<img width="600" alt="image" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/28069ef3-80a9-4fc8-af3a-397df4f967f7">

## Real Time PCR (rtPCR)
Real-time PCR, also known as quantitative PCR (qPCR), is a powerful technique used to measure the expression level of a specific gene in real-time. Unlike traditional PCR, which simply amplifies DNA without providing quantitative information, real-time PCR allows researchers to accurately determine the amount of a specific RNA (gene transcript) present in a sample. 
Real-time PCR is performed using a machine called a real-time PCR thermal cycler. The machine rapidly cycles through different temperature stages, including denaturation, annealing, and extension, allowing DNA amplification to occur. During the PCR reaction, fluorescent signals emitted by the fluorescent probes are measured in real-time to detect expression level of a target gene. 

<img width="360" alt="image" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/f576facc-bd48-4376-8aa5-54753da1c9d6">

### Efficiency in rtPCR 
>> In rtPCR, scientists assume that the efficiency of the process stays constant. But studies have shown that this isn't always true. The efficiency actually changes as the PCR progresses through its cycles. By understanding how efficiency changes during rtPCR, we can develop better methods for quantifying gene expression levels. **Creating a mathematical model of rtPCR helps us understand these changes and leads to more accurate ways to measure efficiency from rtPCR data.** 

#### And this is what we are going to do in this project :) 

## Building a mathematical model of the annealing stage of rtPCR

For this project we are going to model the annealing stage of rtPCR using a mathematical model created by Jana L. Gevertz, Stanley M. Dunn, Charles M. Roth in the paper "Mathematical model of real-time PCR kinetics", that you can find [here:](https://analyticalsciencejournals.onlinelibrary.wiley.com/doi/abs/10.1002/bit.20617)

During annealing, primer 1 (P1) binds to template 1 (T1) to form a hybrid molecule (H1), represented by the equation: P1 + T1 ↔ H1
Similarly, primer 2 (P2) binds to template 2 (T2) to form another hybrid molecule (H2), represented by the equation: P2 + T2 ↔ H2
These equations represent the reversible nature of the annealing process, where the primers can bind and dissociate from the templates depending on the reaction conditions.
In addition to the desired primer-template hybridization reactions, other reactions can occur during the annealing stage of PCR. These include the re-annealing of complementary template strands (T1 + T2 ↔ HT) and the formation of primer-dimers (P1 + P2 ↔ D). Therefore, a total of four reactions can occur simultaneously during this stage. 
These 4 reactions are modeled using thermodynamics (equilibrium) or kitenic equations 

<img width="700" alt="Screenshot 2024-05-08 at 8 03 46 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/adb96f0d-46eb-4894-b576-eddc02572710">

### Equilibrium Model

>> In the steady-state thermodynamic model of the annealing stage of PCR, the total concentration of all products involved in active reactions is tracked. A mass balance is performed on the reactions to derive equations that represent the conservation of mass for each reactant and product. In these equations, [X]_T represents the total concentration of product X, which includes the concentration of free molecules and any complexes formed with other reactants. The equations describe the balance of primer and template molecules as they participate in hybridization reactions (H1 and H2 formation) as well as other potential reactions such as re-annealing of complementary template strands (U formation) and primer-dimer formation (D).

<img width="603" alt="Screenshot 2024-05-08 at 8 08 17 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/73ff75df-48d7-450f-969e-b20a21420211">

#### Reactions Proceed to Equilibrium 
Here, each of the reactions (R1)–(R4) is assumed to proceed to equilibrium. For each reaction, the equilibrium constant is the ratio of reactant to product concentrations which is fixed (written for dissociation of each hybrid). 

<img width="603" alt="Screenshot 2024-05-08 at 8 10 20 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/f3d3eb27-d110-4741-92af-aaf0399b5528">

#### If the reactions do not proceed to equilibrium, we must follow their progression in time using kinetic equations

### Kinetic Model 
In the kinetic model, the equilibrium constant from previous equations is now the ratio of kinetic dissociation and association rate constants, where the lower case k denotes a rate rather than an equilibrium constant and the d and a in the subscripts denote dissociation and association, respectively. 

<img width="683" alt="Screenshot 2024-05-08 at 8 17 42 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/3e68ec53-d227-4a0b-87c5-f37fb5f7cab9">

By applying mass action kinetic balances to each species, the reactions are described by a nonlinear system of **eight differential equations:**

### Kinetic Differential Equations:
<img width="830" alt="Screenshot 2024-05-08 at 8 19 42 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/ae90dad9-6ba6-4a4c-afa0-d75b61b27470">

### Efficiency of the Annealing Stage
By understanding how the concentrations of these molecules change over time, we could then calculate the efficiency of the annealing stage, which measures **how effectively the primers bind to the templates to form hybrid molecules**. This efficiency calculation provides valuable insights into the performance of the PCR reaction and helps optimize reaction conditions for efficient amplification of the target DNA sequence. 
>> The efficiency of the annealing stage, εann(n), can be calculated by comparing the amount of hybrids after the nth annealing stage to the total amount of template present throughout the nth annealing stage 
which [H1] and [H2] can be found by solving the nonlinear system of eight equations.

<img width="476" alt="image" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/813f8973-088c-4d82-9a16-2ab0eff368ec">

#  <img width="40" alt="image" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/21becf4c-1a68-47b6-afff-49f3de6a1345"> Python Model 

For this project I will atempt to build my model using Python. **Why Python?** It's relatively easy to use and it has built in functions that can make the modulation a little easier. 

#### First, we are going to start importing necessary libraries: 

```python
import numpy as np
from scipy.integrate import solve_ivp
import matplotlib.pyplot as plt
```

**For the parameters, we are going to use values from Table 1 in the paper, so that at the end we can compare our results with theirs and see if the model performed correctly:**
```python
P1_T = 1e-6  # M
P2_T = 1e-6  # M
T1_T_min = 1e-14  # M
T1_T_max = 1e-10  # M
T2_T_min = 1e-14  # M
T2_T_max = 1e-10  # M
KH1 = 5.5531e-13  # M
KH2 = 8.1493e-11  # M
KU = 0  # M
KD = 1e-2  # M
kaH1 = 1e6  # M^-1 s^-1
kaH2 = 1e6  # M^-1 s^-1
kaU = 1e6  # M^-1 s^-1
kaD = 1e6  # M^-1 s^-1
kdH1 = 5.5531e-7  # s^-1
kdH2 = 8.1493e-5  # s^-1
kdU = 0  # s^-1
kdD = 1e4  # M^-1 s^-1
Km = 1.5e-9  # M
kcat = 0.17  # M^-1 s^-1
kdeg = 1.9e-4  # s^-1
tden = 1  # s
text = 15  # s
```

## Equilibrium Model 
To solve the system of nonlinear equations in the equilibrium model, we are going to employ the **Newton-Raphson method**, which is an iterative numerical technique used to find successively better approximations to the roots (or zeroes) of a real-valued function. It's particularly useful for solving equations where an analytical solution is difficult or impossible to obtain. In our model we specifically used the **'root'** function from the **scipy.optimize** module in Python. The root function is a generalization of the Newton-Raphson method and is suitable for solving systems of nonlinear equations.

```python
# Define the equations
def equations(X):
    P1, P2, T1, T2, H1, H2, U, D = X
    return [
        P1_T - (P1 + H1 + D),
        P2_T - (P2 + H2 + D),
        T1_T_max - (T1 + H1 + U),
        T2_T_max - (T2 + H2 + U),
        KH1 - (P1 * T1 / H1),
        KH2 - (P2 * T2 / H2),
        KU - (T1 * T2 / U),
        KD - (P1 * P2 / D)
    ]

# Initial guess within reasonable bounds, had to adjust this like 50 times to get reasonable final concentrations value
initial_guess = [1e-6, 1e-6, 1e-10, 1e-10, 1e-10, 1e-10, 1e-10, 1e-11]

# Solve the equations using root method (generalization of Newton-Raphson)
solution = root(equations, initial_guess)

P1, P2, T1, T2, H1, H2, U, D = solution.x # Extracting solutions

# Calculate efficiency using formula provided
efficiency_ann = 0.5 * ((H1 / T1_T_max) + (H2 / T2_T_max)) * 100

print("Concentrations:")
print(f"P1: {P1} M")
print(f"P2: {P2} M")
print(f"T1: {T1} M")
print(f"T2: {T2} M")
print(f"H1: {H1} M")
print(f"H2: {H2} M")
print(f"U: {U} M")
print(f"D: {D} M")
print(f"Annealing Efficiency: {efficiency_ann:.2f}%")
```

## Fine-tuning Process 🔎
At first, I tried setting initial guessing for the concentrations of P1,P2,T1,T2,H1,H2, U and D. The outcome of that was very irrational: 

<img width="323" alt="Screenshot 2024-05-08 at 10 40 38 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/e3150387-9fb9-472e-9b35-bee3a7e5925d">

>> Concentrations represent the amount of a substance present in a given volume, and by definition, they cannot be negative. Negative concentrations obtained from the model calculation indicate that the solver has encountered numerical instabilities or has converged to a solution that does not accurately represent the physical system. This can happen when the solver encounters difficulties in finding a valid solution due to the complexity of the equations or inappropriate initial conditions. 

To solve this, I tried implementing other methods available within the scipy.optimize.root module, such as the **hybrid Powell method ('hybr')**, **the Levenberg-Marquardt algorithm ('lm')**, or the **Broyden's method ('broyden1' or 'broyden2')**.

#### ☹️ unfortunately, that just made things worse:

<img width="318" alt="Screenshot 2024-05-08 at 10 48 43 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/ce62cd5e-aa05-460c-a6eb-8ed6b5bac024">

### 💡 Eventually, it occured to me that I should be focusing my attention on the initial guesses of the concentrations

For a successful high-efficiency PCR, you generally want a **higher concentration** of the components that **contribute** directly to amplifying your target DNA (amplicon) and **lower concentrations** of components that might **interfere** with or compete against this amplification

#### Higher concentration desired:
- **H1 and H2:** These are the primers specific to the target DNA sequences. They should be present at a concentration sufficient to anneal specifically to the target sequences and initiate amplification.
- **T1 and T2:** They should also be present in high concentration since they are responsible for extending the primers and synthesizing new DNA strands during each cycle of PCR.
- **U (hybrid)**: They should be present at a sufficient concentration for efficient DNA synthesis.

#### Lower concentration desired:
- **P1 and P2:** These are the primers not specific to the target sequences. While they may be necessary for certain PCR protocols, having them at a lower concentration can help reduce non-specific amplification.
- **D (primer-dimer):** Primer dimers are unintended products formed when primers anneal to each other rather than to the target DNA. Keeping their concentration low helps minimize their formation, which can interfere with the amplification of your target sequence.

### Implementing changes based on that logic yielded to much greater improvements: 

<img width="280" alt="Screenshot 2024-05-08 at 11 02 49 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/292d2305-c4a3-4f93-ac24-95fb992cae6b">


### 📈 Plotting the Efficiency over 35 cycles
In the paper studied they plot the efficiency and see its behavior over 35 cycles. I decided to generate the same plot and compare it with the plot from the paper:

```python

# Initial guess
initial_guess = [1e-6, 1e-6, 1e-10, 1e-10, 1e-10, 1e-10, 1e-10, 1e-11]

# Number of cycles specified in the paper
num_cycles = 35

# Initialize arrays to store efficiencies
annealing_efficiencies = []

# Simulate the system for each cycle and calculate efficiency
for cycle in range(1, num_cycles + 1):
    # Solve equations for current cycle
    solution = root(equations, initial_guess)
    concentrations = solution.x
    
    # Extract concentrations
    P1, P2, T1, T2, H1, H2, U, D = concentrations
    
    # Calculate efficiency for current cycle
    efficiency_ann = 0.5 * ((H1 / T1_T_max) + (H2 / T2_T_max)) * 100
    
    # Store efficiency
    annealing_efficiencies.append(efficiency_ann)
    
    # Update initial guess for next cycle
    initial_guess = concentrations

# Plot annealing efficiencies
plt.figure(figsize=(8, 6))
plt.plot(range(1, num_cycles + 1), annealing_efficiencies, marker='o', linestyle='-')
plt.xlabel('Cycle')
plt.ylabel('Annealing Efficiency (%)')
plt.title('Cycle Dependent Efficiencies')
plt.grid(True)
plt.show()
```

## My plot: 

![plot equilibrium ](https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/89253aca-fad4-4237-86dd-62d218bb6f2c)

## Paper's plot: 

<img width="471" alt="Screenshot 2024-05-08 at 11 19 48 AM" src="https://github.com/yasminsoltani/numerical_analysis.md/assets/103854541/a0831e25-564a-4861-986d-ef80d6468075">

In both graphs, cycle efficiency drops to 0 after some cycle and remains 0 afterwards. If the efficiency drops to 0, it generally indicates that the **PCR reaction has reached completion**, meaning that all available template DNA has been amplified and there are no more target sequences left to amplify. In this case, the PCR reaction has saturated, and further cycling will not lead to additional amplification. 

### Based on this, we could humbly announce that our equilibrium model demonstrated successful performance 🥳














