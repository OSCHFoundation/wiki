OSCH的Token的创造方法非常便捷，只需要在OSCH实验室里完成简单的几步，即可发行属于自己的Token。   
假设制作一个HUG代币。HUG创造的数量是5000个，OSCH网络可以确保了它不会再被创造，所以不必去考虑HUG通货的膨胀问题。  

# 创造一个发行账户
使用实验室生成发行账号的密钥对,或者通过编程的方式也可以生成新账户   
向新生成的公钥里转一笔最小1个OSCH的币，用于创建新账户
!['密钥对'](https://github.com/OSCHFoundation/wiki/raw/master/image/Tokens%20on%20%20OSCH%201.png)
# 创建分发账户
使用上面相同的方法创建分发的账户
# 和发行账户建立信任
我们需要在实验室中使用变更信任操作
!['change Trust'](https://github.com/OSCHFoundation/wiki/raw/master/image/Tokens%20on%20OSCH%202.png)
# 创建Token
分发帐户信任发行帐户的HUG，通过发行帐户发送需要发行HUG的总量给分配帐户，就可以创建HUG。
发布Token的OSCH实验室


# 限制供应
TOken已经创建了，你可以告诉人们它的全部内容。   
现在你可能想向全世界证明你不会用你的代币涌入市场。
OSCH给你提供了最简单的方法————锁定发行帐户，使其无法再进行交易。
您可以使用OSCH的多重标记功能执行此操作。您只需更改帐户上主签名者的权重即可。
现在该帐户被锁定，您可以确定世界上只有5000个HUG。
我发布了上面的密钥，所以请随意尝试，以确保它不能发出更多的Token。 
