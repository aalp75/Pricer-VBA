# Pricer-VBA

This is a simple pricer for Bonds, Interest Rate Swap and Total Return Swap developped in VBA.

Inputs are the caracteristics of the contract and the spot yield curve (one for discount and one for floating rate).

The forward rate for the period $[T_1,T_2]$ is calculted by the formula 
$\begin{align*} R_{T_1}(T_2) = \frac{1}{T_2-T_1}\left[ T_2R_0(T_2) - T_1R_0(T_1) \right] \end{align*}$ and the discount factor is calculated as continuous rate $D(t,T)=e^{(T-t)R_t(T)}$

**1. Bonds**

**1.1 Caracterisitics**

- Valuation date
- Type (Fixe or variable)
- Nominal
- Issuer date
- Maturity
- Frequency of coupons (by year)
- Fixed rate
- Float rate
- Calendar (French or UK)
- Convention close day(next, previous, closest)
- Convention of day computing (ACT/ACT, ACT/360)
- Interpolation method of yield curbe (Linear, Quadratic)

**1.2 Additional Features**

You can compute the clean price and the dirty price. You can also compute the actuarial rate and the duration of the bond. The actuarial rate is fine by dichotomy.

**2. Interest Rate Swap**

**2.1 - Caracteristics**

Same as Bonds. You do not must have the same frequency on the 2 legs.

**2.2 Additional Features**

You can compute the swap rate which is done by dichotomy

**3. Total Return Swap**

Compute the price of a TRS by pricing the premium leg and pricing the Underlying Bonds at 2 differents dates.

![alt text](https://github.com/aalp75/Pricer-VBA/blob/main/Example.png)

