# PN-Net
## reproduce paper PN-Net:Conjoined Triplet Deep Network for Learning Local Image Descriptor
# 有2点需要声明
# There are two important detail needed to be clarified
## 1 In author raw Lua code work ,I couldn't explictly find there is a batchnormlization.Maybe I dont konw how to use Lua and Torch
## 1 作者开源的Lua源码中没有显示的发现作者使用的BN,但是在复现中使用了BN
### The reason to use BN
Because in the procedure of optimization,there is always a gradient explode and thus cant continue to training,I dont kown why .I provide two solutions:First,use gradient clip in the train code which i comment it as i have used BN,once use BN,there is no optimization problem.Second,use BN

# I only do training on Brown Dataset Liberty 
# testing on the other two subsets Notredame and Yosemite
# results
### Notredame ROC
![image](https://github.com/lovekittynine/PN-Net/blob/master/%E5%AE%9E%E9%AA%8C%E8%AE%B0%E5%BD%95/pnsoft_loss_roc_notredame.png)
### Yosemite ROC
![image](https://github.com/lovekittynine/PN-Net/blob/master/%E5%AE%9E%E9%AA%8C%E8%AE%B0%E5%BD%95/pnsoft_loss_roc_yosemite.png)
### result
![image](https://github.com/lovekittynine/PN-Net/blob/master/result.png)
### We find there are 2.5 points higer than raw paper.Because we use 50w pairs,however original paper using 120w pairs.
