#Plot the optimal region

import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
from scipy.optimize import linprog

# Construct lines
# x > 0
x = np.linspace(0, 30, 2000)
# y >= 3
y1 = (x*0) + 3
# 2y <= 25 - x
y2 = (25-x)/2.0
# 4y >= 2x - 8 
y3 = (2*x-8)/4.0
# y <= 2x - 5 
y4 = 2 * x -5

# Make plot
plt.plot(x, y1, label=r'$y\geq3$')
plt.plot(x, y2, label=r'$2y\leq25-x$')
plt.plot(x, y3, label=r'$4y\geq 2x - 8$')
plt.plot(x, y4, label=r'$y\leq 2x-5$')
plt.xlim((0, 30))
plt.ylim((0, 11))
plt.xlabel(r'$x$')
plt.ylabel(r'$y$')

# Fill feasible region
y5 = np.minimum(y2, y4) 
y6 = np.maximum(y1, y3)
plt.fill_between(x, y5, y6, where=y5>y6, color='green', alpha=0.5)
plt.legend(bbox_to_anchor=(1.05, 1), loc=2, borderaxespad=0.)
