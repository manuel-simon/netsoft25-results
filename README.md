# netsoft25-results

To approximate parameters $a_{rx}, a_{tx}, b_{rx}, b_{tx}$ we conducted measurements (1500-byte packets) to determine $n$ by using different $r_{rx}$ using linear-least squares.
Using the model, measured values for $r_{tx}$ can be split into the I/O and processing times.
On our setup, we measure these times for different $r_{rx}$ and apply the model to calculate the general shares of I/O and processing time for the packets.
The following table provides all model parameters for all experiments conducted in the paper.


## Model Parameters

Model parameters, $r'_{max}$ is the calculated maximum rate, used for validation of the model, 1500 Byte packet size

| CPU | Mode | Driver | $a_{\text{rx}} + a_{\text{tx}}$ | $b_{\text{rx}} + b_{\text{tx}}$ | $a_{\text{process}}$ | $b_{\text{p}}$ | $r_{\text{max}}$ | $r_{\text{max}}'$ |
| -- | -- |  -- | -- | -- | -- | -- | -- | -- |
| EPYC 9354 |  | AF_XDP | 3.008 | 1.420 | -0.063 | 0.400 | 0.52 | 0.52 |
| EPYC 9354 |  | ICE | -0.011 | 0.010 | 0.072 | 0.441 | 2.06 | 2.21 |
| EPYC 9354 | SNP | AF_XDP | 10.193 | 1.539 | -0.080 | 0.408 | 0.44 | 0.44 |
| EPYC 9354 | VM | AF_XDP | 6.137 | 1.200 | -0.108 | 0.406 | 0.55 | 0.56 |
| EPYC 9354 | VM | ICE | -0.001 | 0.011 | -0.024 | 0.438 | 2.06 | 2.23 |
| EPYC 7543 |  | AF_XDP | 2.727 | 1.842 | -0.100 | 0.424 | 0.42 | 0.43 |
| EPYC 7543 |  | ICE | 0.085 | 0.012 | -0.027 | 0.461 | 1.96 | 2.11 |
| EPYC 7543 | SNP | AF_XDP | 10.565 | 1.588 | -0.071 | 0.429 | 0.42 | 0.43 |
| EPYC 7543 | VM | AF_XDP | 6.200 | 1.261 | -0.097 | 0.431 | 0.53 | 0.53 |
| EPYC 7543 | VM | ICE | 0.071 | 0.012 | -0.013 | 0.458 | 1.97 | 2.12 |
| Xeon 6421N |  | AF_XDP | 1.888 | 0.991 | 0.007 | 0.341 | 0.68 | 0.72 |
| Xeon 6421N |  | ICE | 0.000 | 0.000 | -0.066 | 0.378 | 2.28 | 2.66 |
| Xeon 6421N | SGX | AF_XDP | 2.056 | 1.039 | 0.237 | 4.098 | 0.19 | 0.19 |
| Xeon 6421N | SGX | ICE | 0.298 | -0.004 | 46.199 | 2.249 | 0.24 | 0.27 |
| Xeon 6312U |  | AF_XDP | 1.630 | 0.865 | -0.070 | 0.400 | 0.74 | 0.76 |
| Xeon 6312U |  | ICE | -0.011 | 0.003 | -0.071 | 0.417 | 2.14 | 2.40 |
| Xeon 6312U | SGX | AF_XDP | 2.048 | 0.896 | 0.319 | 4.964 | 0.17 | 0.17 |
| Xeon 6312U | SGX | ICE | 0.229 | -0.001 | 85.392 | 1.560 | 0.20 | 0.24 |


