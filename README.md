#Objective: To integrate 1d Swift-Hohenberg (SH) equation with periodic boundaries.

##Method used: spectral method using Fourier modes in spatial dimension, time integration is performed using: second-order Adams-Bashforth + Crank-Nicholson (implicit treatment of linear terms and explicit treatment to non-linear terms) 

	The SH equation used-

	du/dt = ru - (qc^2 - (d/dx)^2)^2u + f(u)
	where, r = bifurcation parameter = 0.2 (we choose an arbitary value)

	qc = characteristic wavenumber = 1.0 (we choose q_c to be unity for infinite domain)

	f(u) = b_2*u^2	-u^3 (we choose the model SH23, where b_2 is a constant > 0) 

#After substuting the respective values of constant the equation solved below appears as -

	du/dt = (r-1)u - (1 - 2*((d/dx)^2)) + (d/dx)^4))u + b_2*u^2 - u^3

#Though one can play around changing SH23 to SH35
##This is a very basic code from which I start learning about spectral and pseudo spectral methods.

Reference: 1d-Kuramoto-Sivashinksy equation (will be shortly uploaded https://github.com/PratikAghor)
