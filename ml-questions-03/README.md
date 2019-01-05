# 03. VC 부등식에 대한 다음 물음들에 대해 답하여라.

- VC 부등식에 대해 설명하라. VC Bound란 무엇인가?
- VC 부등식에서, Hypothesis Space의 크기를 감소시킬 때 발생하는 현상에 대해 설명하라.
- Structural Risk Minimization이란 무엇인가? ERM과 어떻게 다른가?
  - ER (Empirical Risk) = the loss function value of the model hypothesis function and real values
  - SR (Structural Risk) = ER + the complexity of the model
  - ERM (Empirical Risk Minimization): Minimizing ER value
  - SRM (Structural Risk Minimization): Minimizing SR value
  - Doing only ERM, it results in the over-fitting.
  - To prevent over-fitting, we need to do SRM. (Regularization)
  - https://mc.ai/empirical-structural-risk-minimization/