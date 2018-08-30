OSCH的Token的创造方法非常便捷，只需要在OSCH实验室里完成简单的几步，即可发行属于自己的Token。   
假设制作一个HUG代币。HUG创造的数量是5000个，OSCH网络可以确保了它不会再被创造，所以不必去考虑HUG通货的膨胀问题。  

# 创造一个发行账户
使用实验室生成发行账号的密钥对,或者通过编程的方式也可以生成新账户   
向新生成的公钥里转一笔最小1个OSCH的币，用于创建新账户
!['密钥对'](https://github.com/OSCHFoundation/wiki/raw/master/image/Token%20s%20on%20%20OSCH%201.png)
# 创建分发账户
使用上面相同的方法创建分发的账户
# 和发行账户建立信任
我们需要在实验室中使用[变更信任操作](https://www.stellar.org/laboratory/#txbuilder?params=eyJhdHRyaWJ1dGVzIjp7InNvdXJjZUFjY291bnQiOiJHQ1FVVjdXQTRTUDNMTlRSRE9CU1VSRU5YNldBNUpVN1E1QjU0WTVJMkc0SVJUR0cySVo2TTcyTSIsInNlcXVlbmNlIjoiNDg4NTI1Mzg1NzI2Njg5MjkifSwib3BlcmF0aW9ucyI6W3siaWQiOjAsImF0dHJpYnV0ZXMiOnsic291cmNlQWNjb3VudCI6IiIsImFzc2V0Ijp7InR5cGUiOiJjcmVkaXRfYWxwaGFudW00IiwiY29kZSI6IkhVRyIsImlzc3VlciI6IkdENVQ2SVBSTkNLRk9IUVdUMjY0WVBLT1pBV1VNTVpPTFpCSjZCTlFNVUdQV0dSTEJLM1U3Wk5QIn0sImxpbWl0IjoiNTAwMCJ9LCJuYW1lIjoiY2hhbmdlVHJ1c3QifV19&network=public) 
!['change Trust'](https://github.com/OSCHFoundation/wiki/raw/master/image/Tokens%20on%20OSCH%202.png)
# 创建Token
分发帐户信任发行帐户的HUG，通过发行帐户发送需要发行HUG的总量给分配帐户，就可以创建HUG。
发布Token的[OSCH实验室](https://www.stellar.org/laboratory/#txbuilder?params=eyJhdHRyaWJ1dGVzIjp7InNvdXJjZUFjY291bnQiOiJHRDVUNklQUk5DS0ZPSFFXVDI2NFlQS09aQVdVTU1aT0xaQko2Qk5RTVVHUFdHUkxCSzNVN1pOUCIsInNlcXVlbmNlIjoiNDg4NTI1NzcyMjczNzQ1OTMifSwib3BlcmF0aW9ucyI6W3siaWQiOjAsImF0dHJpYnV0ZXMiOnsiZGVzdGluYXRpb24iOiJHQ1FVVjdXQTRTUDNMTlRSRE9CU1VSRU5YNldBNUpVN1E1QjU0WTVJMkc0SVJUR0cySVo2TTcyTSIsImFzc2V0Ijp7InR5cGUiOiJjcmVkaXRfYWxwaGFudW00IiwiY29kZSI6IkhVRyIsImlzc3VlciI6IkdENVQ2SVBSTkNLRk9IUVdUMjY0WVBLT1pBV1VNTVpPTFpCSjZCTlFNVUdQV0dSTEJLM1U3Wk5QIn0sImFtb3VudCI6IjUwMDAifSwibmFtZSI6InBheW1lbnQifV19&network=public)  
!['发布HUG'](https://github.com/OSCHFoundation/wiki/raw/master/image/Tokens%20on%20OSCH%204.png)
# 发布你的Token信息
!['发布HUG的信息'](https://github.com/OSCHFoundation/wiki/raw/master/image/Tokens%20on%20OSCH%203.png)   
为了证明我是创建此令牌的人，我还使用我的keybase公钥对doc进行签名。我把这个文档发布到IPFS。   
你可以在这里看到完整的文档https://ipfs.io/ipfs/QmWZzqxe9kHGmgFmquGQQTyrpJ4H7hocdzUS6DPmTNCQC8    
现在我们要将令牌描述的IPFS哈希附加到发行帐户。我们使用管理数据操作来完成此操作。这是实验室里的这笔交易。
# 限制供应
TOken已经创建了，你可以告诉人们它的全部内容。   
现在你可能想向全世界证明你不会用你的代币涌入市场。
OSCH给你提供了最简单的方法————锁定发行帐户，使其无法再进行交易。
您可以使用OSCH的多重标记功能执行此操作。您只需更改帐户上主签名者的权重即可。
现在该帐户被锁定，您可以确定世界上只有5000个HUG。
您可以在此处看到发行帐户被锁定：https：//horizo​​n.stellar.org/accounts/GD5T6IPRNCKFOHQWT264YPKOZAWUMMZOLZBJ6BNQMUGPWGRLBK3U7ZNP

我发布了上面的密钥，所以请随意尝试，以确保它不能发出更多的Token。
# 分发Token
现在您的Token已经存在，一切都已设置好。最后一步是让他们掌握在人们手中。当然，有很多方法可以做到这一点。Stellar的一大特色是它具有内置的分散交换。让HUG以一种自然方式为他们提供报价。


> 参考地址：
[Tokens on stellar](https://www.stellar.org/blog/tokens-on-stellar/)  
