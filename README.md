## 🧰 How to Use This Template    

Click the green **"Use this template"** button at the top of the page, then choose **"Create a new repository"**.   

This will create your own copy of this project, which you can modify freely — no need to fork!   

 
<p align="center">
  <img src="./images/SHG-banner.png" alt="SHG Logo">
</p>


<h1 align="center">SHG-CW-G-Fields-Ideal</h1>

<div align="center">

| **Term** | **Definition** |
|----------|----------------|
| **SHG** | Second Harmonic Generation |
| **CW** | Continuous Wave |
| **G** | Gaussian |
</div>

&nbsp;

<div align="center">

Article title:       
**Temperature increase effects on a double-pass cavity type II second-harmonic generation: a model for depleted Gaussian continuous waves**
</div>

&nbsp;

---

***Table of Contents***

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#1-about-this-repository"><i><b>1. About this repository</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-getting-started"><i><b>2. Getting Started</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#3-how-to-cite-us"><i><b>3. How to Cite Us</b></i></a>
</div>
&nbsp;


<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#4-contact-information"><i><b>4. Contact Information</b></i></a>
</div>
&nbsp;

---    

## 1. About this repository

This repository contains the **Toolkit for Modeling of Second Harmonic Electric-Field Distribution in KTP Crystal: Continuous-Wave Gaussian Second Harmonic Generation**, an open-source toolkit for investigating the effect of temperature increase on the efficiency of second-harmonic generation (SHG) processes.

### Toolkit Overview

The toolkit implements a comprehensive depleted wave model that describes the continuous-wave SHG process with fundamental Gaussian waves in a double-pass cavity type II configuration. The model solves six coupled equations to generate the second harmonic of a Gaussian fundamental wave, accounting for fundamental beam depletion rather than using the conventional non-depleted assumption.

The toolkit models the critical effect of temperature increase in the nonlinear crystal due to optical absorption by incorporating mismatched phase arising from changes in refractive indices into the coupled equations. This approach enables the investigation of how SHG efficiency decreases when the crystal temperature increases by 5, 10, and 15 K, revealing dramatic reductions in efficiency due to small temperature changes.

The implementation features a homemade code written in Intel Fortran with compiled kernels, built-in benchmark reporting, and reproducible pipelines. The toolkit generates comprehensive datasets with spatiotemporal field distributions and efficiency analyses, showing excellent agreement with experimental data. This toolkit was used to solve the modeling problem described in the research article **"Temperature increase effects on a double-pass cavity type II second-harmonic generation: a model for depleted Gaussian continuous waves"**.  

```
Folder PATH listing
+---citation                    <-- Contains research papers and citations
│       1_Heat-Equation_Cont…   <-- Heat equation analytical solutions
│       2_Heat-Equation_Cont…   <-- Heat equation continuous wave
│       3_Heat-Equation_Puls…   <-- Heat equation pulsed wave
│       4_Phase-Mismatch_Pul…   <-- Phase mismatch pulsed wave
│       5_Ideal_Continuous-W…   <-- Ideal continuous wave solutions
│       6_Ideal_Pulsed-Wave_…   <-- Ideal pulsed wave Bessel-Gaussian
│       7_Coupled_Continuous…   <-- Coupled continuous wave equations
│       README.md               <-- Citation guidelines and references
│
+---images                      <-- Contains project images and logos
│       SHG-banner.png          <-- Project banner image
│
+---results                     <-- Contains simulation output files
│       elec1-2-3.plt           <-- Combined electric field plots
│       elec1_m-z.plt           <-- Electric field 1 minus z plots
│       elec1_p-z.plt           <-- Electric field 1 plus z plots
│       elec2_m-z.plt           <-- Electric field 2 minus z plots
│       elec2_p-z.plt           <-- Electric field 2 plus z plots
│       elec3_m-z.plt           <-- Electric field 3 minus z plots
│       elec3_p-z.plt           <-- Electric field 3 plus z plots
│
+---src                         <-- Contains source code files
│       Code_SHG-CW-G-Fields…   <-- Main Fortran implementation
│
│       Article_SHG-CW-G-Fie…   <-- Main research article PDF
│       CITATION.cff            <-- Citation metadata file
│       LICENSE                 <-- Project license information
│       README.md               <-- Project documentation
```


## 2. Getting Started

### 2.1. Prerequisites
- **Fortran Compiler** (gfortran, Intel Fortran, or similar)
- **Text Editor** (VS Code, Cursor, or any Fortran-capable editor)
- **PDF Reader** (for accessing research papers)
- **Git** (for cloning the repository)
- **Plotting Software** (Gnuplot, Python matplotlib, or similar for visualizing results)

### 2.2. Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/Second-Harmonic-Generation/SHG-CW-G-Fields-Ideal.git
   cd SHG-CW-G-Fields-Ideal
   ```

2. **Explore the Research Papers**
   - Navigate to the `citation/` folder
   - Read the main research paper: `Article_SHG-CW-G-Fields-Ideal.pdf`
   - Review additional papers for comprehensive understanding

3. **Compile and Run the Toolkit**
   ```bash
   cd src
   gfortran -o shg_fields Code_SHG-CW-G-Fields-Ideal.f90
   ./shg_fields
   ```

4. **Analyze Results**
   - Check the `results/` folder for output files
   - Examine `.plt` files for electric field distributions
   - Use plotting software (Gnuplot, Python matplotlib, etc.) to visualize results

5. **Run Parameterized Scenarios** (Optional)
   - Edit the Fortran source code to change simulation parameters
   - Explore different scenarios:
     - Temperature increases (5, 10, 15 K)
     - Different crystal configurations
     - Various pump powers and beam parameters
   - Recompile and run to compare results with published findings



## 3. How to Cite Us
Please refer to the [**citation**](./citation/) folder for accurate citations. It contains essential guidelines for accurate referencing, ensuring accurate acknowledgement of our work.


  
## 4. Contact Information

For questions not addressed in the resources above, please connect with [Mostafa Rezaee](https://www.linkedin.com/in/mostafa-rezaee/) on LinkedIn for personalized assistance.
