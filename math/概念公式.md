### Information theory

- 自信息： $\mathrm{I}(X) = -\ln(\mathrm{P}(X)$

事件發生概率的量度。事件發生的概率越低，信息量越大。

- 熵

 $H(X) = \mathrm{E}[\mathrm{I}(X)] = \mathrm{E}[-\ln(\mathrm{P}(X))]$

熵是自信息的期望值，是對不確定性的度量。熵越高，则能传输越多的信息，熵越低，则意味着传输的信息越少。

$\mathrm{H} (X)=\sum _{{i}}{{\mathrm  {P}}(x_{i})\,{\mathrm  {I}}(x_{i})}=-\sum _{{i}}{{\mathrm  {P}}(x_{i})\log _{b}{\mathrm  {P}}(x_{i})}$

- 聯合信息熵

$\Eta(X,Y)=-\sum_{X}\sum_{Y}P(x,y)log P(x,y)$

- 條件信息熵

$\Eta(X,Y)=\Eta(X|Y)+\Eta(Y)=\Eta(Y|X)+\Eta(X)]$

$\Eta(X|Y)=-\sum_{X}\sum_{Y}P(x,y)log P(x|y)$

条件信息熵H(X|Y )用来度量在收到随机变量Y 提供的信息后，随机变量X仍然存在的不确定性

- 互信息

$I(X;Y)=\Eta(X)-\Eta(X|Y)=\sum_{X}\sum_{Y}P(x,y)log(\dfrac{P(x,y)}{P(x)P(y)})$

互信息I(X;Y )用来描述随机变量Y 提供的关于X的信息量的大小

- 條件互信息

$I(X;Y|Z)=\sum_{X}\sum_{Y}\sum_{Z}P(x,y,z)log(\dfrac{P(x,y,z)P(Z)}{P(x,z)P(y,z)})=\sum_{X}\sum_{Y}\sum_{Z}P(x,y,z)log(\dfrac{P(x,y|z)}{P(x|z)P(y|z)})$

