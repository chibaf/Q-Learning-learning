# Q-Learning-learning

<ul>
import torch<br>
import torch.nn as nn<br>
import torch.nn.functional as F<br>
#<br>
class DQN(nn.Module):
    def __init__(self):<br>
        super(DQN, self).__init__()<br>
        self.l1 = nn.Linear(1, 3)<br>
        self.l2 = nn.Linear(3, 3)<br>
        self.l3 = nn.Linear(3, 2)<br>
    # generating neural netwok layers<br>
    def forward(self, x):<br>
        x = F.relu(self.l1(x)) # the first layer<br>
        x = F.relu(self.l2(x)) # the second layer<br>
        x = self.l3(x) # the third layer<br> 
        return x<br>
</ul>

<img width="600" alt="neuralnet-layers-num" src="https://github.com/user-attachments/assets/2bc46c46-d1ae-4e13-81ca-9b2df60c9cf2" />


## references
深層強化学習(Deep Q Network, DQN)の簡単な例 - 化学系エンジニアがAIを学ぶ
https://schemer1341.hatenablog.com/entry/2019/05/04/002300

Linear — PyTorch 2.7 documentation
https://docs.pytorch.org/docs/stable/generated/torch.nn.Linear.html
