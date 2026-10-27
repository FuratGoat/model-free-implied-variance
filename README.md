# model-free implied variance

A single Jupyter notebook that builds a VIX-style implied variance index for any optionable ETF, at any horizon,
directly from raw end-of-day option quotes.

It derives the theory step by step, from replicating the log contract with puts and calls to discretising the
integral with Simpson's rule, which removes the bias of about $h^2/(6F^2)$ that CBOE's formula leaves in. Every step is
implemented in code and checked against synthetic Black–Scholes, Heston and Merton chains where the true answer is
known. The notebook ends with results on 15 years of SPY, QQQ and IWM option chains.

Open [model_free_implied_variance.ipynb](model_free_implied_variance.ipynb) to read it with all outputs, or run it top
to bottom with `numpy`, `scipy`, `pandas` and `matplotlib` installed.
