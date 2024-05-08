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
mally, in rtPCR, scientists assume that the efficiency of the process stays constant. But studies have shown that this isn't always true. The efficiency actually changes as the PCR progresses through its cycles. By understanding how efficiency changes during rtPCR, we can develop better methods for quantifying gene expression levels. **Creating a mathematical model of rtPCR helps us understand these changes and leads to more accurate ways to measure efficiency from rtPCR data.** 

#### And this is what we are going to do in this project :) 

## Building a mathematical model of the annealing stage of rtPCR

For this project we are going to model the annealing stage of rtPCR using a mathematical model created by Jana L. Gevertz, Stanley M. Dunn, Charles M. Roth in the paper "Mathematical model of real-time PCR kinetics", that you can find [here:](https://analyticalsciencejournals.onlinelibrary.wiley.com/doi/abs/10.1002/bit.20617)







