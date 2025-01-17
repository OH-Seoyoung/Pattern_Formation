# Pattern Formation
- Explorations of pattern formation in fractional partial differential equations
- This is the implementation of paper by Yin et.al. "Pattern formation through temporal fractional derivatives"
- May. 2, 2021 ~ Aug. 1, 2021

&nbsp;
&nbsp;
&nbsp;

## Diffusive prey-predator systems with Holling II functional response
<sup>∂<sup>&eta;</sup>u</sup>/<sub>∂t</sub> = &Delta;u  + u(1-u) - <sup>uv</sup>/<sub>u+&alpha;</sub>  
<sup>∂<sup>&eta;</sup>v</sup>/<sub>∂t</sub> = d&Delta;v  - &gamma; v + <sup>&beta;uv</sup>/<sub>u+&alpha;</sub>

If &eta; = 1, the system degenerates into the temporal first-derivative system, which represents the instantaneous behaviors of the prey and predator.   
The parameters are taken as &alpha; = 0.175, &beta; = 0.95, &gamma; = 0.5, &eta; = 0.8, d = 20. ・・・ (a)
  
### 1. Temporal **first**-derivative system | [Code](https://github.com/OH-Seoyoung/Pattern_Formation/blob/master/Diffusive_prey-predator_systems/First_derivative.m)  
- Forward Euler method in time and Central differences in space (FTCS)
- Zero-flux boundary condition, 1D
  
#### 1) The spatial homogeneous periodic orbits of the prey and predator in 1D.
<div align="">
<img src="https://github.com/OH-Seoyoung/Pattern_Formation/blob/master/Diffusive_prey-predator_systems/figs/orig.jpg?raw=True" width="48%"> <br>
</div>  
  
The parameters are taken as (a).

#### 2) Change diffusion coefficient "d" into 0.1 and length scale "h" into 10.
<div align="">
<img src="https://github.com/OH-Seoyoung/Pattern_Formation/blob/master/Diffusive_prey-predator_systems/figs/change_d_L.jpg?raw=True" width="48%"> <br>
</div>  
  
If we change diffusion coefficient "d" into 0.1, we can observe the fluctuation in time and the small changes in space.  
If "d" and "h" are properly chosen, even first-order derivatives can form patterns.  

&nbsp;
&nbsp;
&nbsp;

### 2. Temporal **fractional**-derivative system | [Code](https://github.com/OH-Seoyoung/Pattern_Formation/blob/master/Diffusive_prey-predator_systems/Fractional_derivative.m)  
- It can form steadily spatial patterns even though its first-derivative counterpart can't exhibit any steady pattern.
- Approximation of the Caputo's derivative by the Grunwald-Letnikov one in time and Central differences in space
- Zero-flux boundary condition, 1D

The differences between 1, 2 with the same parameters implies that the fractional derivative can product steady-state spatial patterns and induce the Turing instability.

&nbsp;
&nbsp;
&nbsp;

## References
```
[1] Yin, Hongwei, and Xiaoqing Wen. "Pattern formation through temporal fractional derivatives." Scientific reports 8.1 (2018): 1-9.
[2] Ciesielski, Mariusz, and Jacek Leszczynski. "Numerical simulations of anomalous diffusion." arXiv preprint math-ph/0309007 (2003).
```
