# Pricer-VBA

This is a simple Pricer for Bonds, Interest Rate Swap and Total Return Swap developped in VBA.

Inputs are the caracteristics of the contract and the spot yield curve (one for discount and one for floating rate).

The forward rate for the period $[T_1,T_2]$ is calculted by the formula $R_{T_1}(T_2) = \frac{1}{T_2-T_1}\left[ T_2R_0(T_2) - T_1R_0(T_1) \right]$ and the discount factor is calculated as continuous rate $D(t,T)=e^{(T-t)R_t(T)}$

1 - Bonds

