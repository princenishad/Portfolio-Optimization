Project One : Portfolio Optimization (CVaR Risk Measure)


Creating the system :

"""
Maximize m.T * x - p * (xp + xm) + xf * rf - delta * (cvar_term)

subject to

1.T * x + a * K + fp * yp + fm * ym + vm * ym + vp * yp + xf = 1

(K, 1, x) belongs to PowerCone (1/beta)

t + 1 * P.T * U/ (1 - alpha) <= gamma

U + t >= -R.T * x

U >= 0

x = xp - xm

y1 + y2 <= 1 ( y is a binary variable)

xp + xm <= 2.0 (gross exposure)

xm <= M * y1

xp <= M * y2

where :

x = array of weights allocated to each scrip
m =  array of mean returns over the time period (h)
p = transaction Cost penalty coeficient
xp = positive fraction of holdings
xm = short selling fraction of holdings
xf = risk free asset allocation
rf = risk free return
delta = risk coeficient
a = Market Impact cost coeficient
K = Market Impact cost auxiliary variable (Height of our cone)
f (p,m) = fixed transaction cost
y (p,m) = Binary variable (signalling transaction) (1 for buy or sell and 0 otherwise)
v (p,m) = Variable transaction cost
t = auxiliary variable 
U = auxiliary variable
R = return scenarios
M = Exposure (Leverage Index)
P = Probabality of each scenario taking place
gamma = Pre-Decided level of CVaR risk
alpha = significance level (0.05)

"""



