# Orthogonality, QR &amp; RoPE

Deck 08 of the [Linear Algebra for AI / ML](https://github.com/BrendanJamesLynskey/LLM_Hub_Linear_Algebra) series.

**Live presentation:** https://brendanjameslynskey.github.io/Linear_Algebra_AI_08_Orthogonality_QR_and_RoPE/

Orthonormal bases are the cleanest way to do anything. QR factorisation is how you build them. And RoPE &mdash; the position encoding inside Llama, Qwen, GPT-NeoX, Mistral, DeepSeek and most modern transformers &mdash; is just a stack of tiny 2&times;2 rotation matrices. Includes an interactive RoPE visualiser.

## What's inside

- Orthonormal sets and orthogonal matrices ($Q^\top Q = I$, $Q^{-1} = Q^\top$)
- Length and angle preservation; why $\kappa(Q) = 1$
- Classical Gram-Schmidt and its numerical limitations
- QR factorisation; least-squares the stable way
- Householder reflectors and Givens rotations &mdash; how production libraries actually compute QR
- Condition number, conditioning of weight matrices, why $Q$ is cheap
- Orthogonal initialisation (Saxe, McClelland &amp; Ganguli 2014)
- 2D rotation matrix algebra; the complex-number reading $R_\theta = e^{i\theta}$
- RoPE construction: rotate each (odd, even) coordinate pair by $m\theta_i$, with $\theta_i$ a geometric frequency comb
- Why $\langle R_m \mathbf{q}, R_n \mathbf{k}\rangle = \mathbf{q}^\top R_{n-m}\mathbf{k}$ &mdash; the relative-position property
- Length extrapolation: Position Interpolation, NTK-aware scaling, YaRN
- Interactive RoPE visualiser (rotate 4 pairs at different frequencies; watch the dot product oscillate)

Single-page HTML, KaTeX-rendered maths, no build step. Open `index.html` directly.
