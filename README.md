# PDE-Datasets-
This repository contains u,x,t datasets for 4 different Partial Differential Equations(PDEs) at various noise levels

## Folders

### [u,x,t](https://github.com/NohanJoemon/PDE-Datasets/tree/main/u%2Cx%2C)
This folder contains u,x,t values for different equations and different SNRs. 


## File names

Files are named as **i_j.pkl** 

**i values:**
<OL>
  <LI>1D Diffusion equation: u_t = (0.15) u_{xx}</LI>
  <LI>Burgers equation:  u_t = (0.1)u_{xx} + (-1)uu_{x}</LI>
  <LI>kdv equation: u_t = (-6)uu_{x} + (-1)u_{xxx}</LI>
  <LI>1D Advection equation: u_t = -0.8 u_{x}</LI>
</OL>

**j values:**

0: Noiseless 
  
1 : SNR =  20000
  
2 : SNR =  15000

3 : SNR =  10000

4 : SNR =  7500

5 : SNR =  5000

6 : SNR =  3000

7 : SNR =  2000

8 : SNR =  1000

9 : SNR =  800

10 : SNR =  500

11 : SNR =  300

12 : SNR =  200

13 : SNR =  100

14 : SNR =  90

15 : SNR =  80

16 : SNR =  70

17 : SNR =  60

18 : SNR =  50

19 : SNR =  40

20 : SNR =  30

21 : SNR =  20

22 : SNR =  10

23 : SNR =  8

24 : SNR =  6

25 : SNR =  5

26 : SNR =  4

27 : SNR =  3

28 : SNR =  2

29 : SNR =  1

### SNR Definition that was used:
u_noisy = u + noise

noise is taken from a normal distribution of mean 0 and variance = var(u)/ SNR

(x,t remains same, noise is added only to u)



**Python code for retrieving u,x and t from the .pkl file: (eg: 2_12.pkl)**


```
path_load = "PDE-Datasets/u,x,t"
file_to_read = open(path_load+"/2_12.pkl", "rb")
loaded_dictionary = pickle.load(file_to_read)
u = loaded_dictionary["u"]
x = loaded_dictionary["x"]
t = loaded_dictionary["t"]
```

