# Adaptive Guard (Academic Overview)

Adaptive Guard is a regime-aware safety layer that modulates trading eligibility by
quantifying market disorder and structural compression. The mechanism integrates
Entropy-based filtering, Bollinger Band Width Compression, and Volatility Z-Score
thresholding to detect adverse microstructure conditions that tend to degrade
signal reliability.

At its core, Entropy-based filtering estimates market entropy as a proxy for
regime noise and directional ambiguity. When Market Entropy exceeds 0.8, the
system refuses to trade to avoid capital erosion in choppy regimes. This hard
gate is designed to prevent execution during periods where probabilistic edge
collapses under stochastic price dispersion.

The entropy term follows Shannon's formulation:
H(X) = -sum p(x_i) log2 p(x_i)
In practice, SignalX computes this over a 60-candle sliding window of price
returns to detect market chaos and suppress trades during disorderly regimes.

Bollinger Band Width Compression provides a structural cue for low-variance
price states, identifying regimes prone to mean-reversion whipsaw and false
breakouts. Compression below a calibrated threshold flags reduced directional
signal-to-noise and raises the risk of drawdown from premature entries.

Volatility Z-Score thresholding complements the above by normalizing short-term
volatility against its recent distribution. Extreme negative z-scores indicate
suppressed volatility and heightened sensitivity to micro shocks, while extreme
positive z-scores mark instability. Adaptive Guard uses these normalized bounds
to defer trades outside statistically favorable volatility windows.

Together, these components form a conservative gating policy: trading proceeds
only when entropy is low, volatility is within a stable band, and structural
compression does not imply a high false-signal regime.
