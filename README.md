# Q-Learning-learning

<ul>
<li>import torch</li>
<li>import torch.nn as nn</li>
<li>import torch.nn.functional as F</li>
<li>#</li>
<li>class DQN(nn.Module):</li>
    <li>def __init__(self):</li>
        <li>super(DQN, self).__init__()</li>
        <li>self.l1 = nn.Linear(1, 3)</li>
        <li>self.l2 = nn.Linear(3, 3)</li>
        <li>self.l3 = nn.Linear(3, 2)</li>
    <li># generating neural netwok layers</li>
    <li>def forward(self, x):</li>
        <li>x = F.relu(self.l1(x)) # the first layer</li>
        <li>x = F.relu(self.l2(x)) # the second layer</li>
        <li>x = self.l3(x) # the third layer</li> 
        <li>return x</li>
</ul>

<img width="600" alt="neuralnet-layers-num" src="https://github.com/user-attachments/assets/2bc46c46-d1ae-4e13-81ca-9b2df60c9cf2" />


## references
深層強化学習(Deep Q Network, DQN)の簡単な例 - 化学系エンジニアがAIを学ぶ
https://schemer1341.hatenablog.com/entry/2019/05/04/002300

Linear — PyTorch 2.7 documentation
https://docs.pytorch.org/docs/stable/generated/torch.nn.Linear.html
