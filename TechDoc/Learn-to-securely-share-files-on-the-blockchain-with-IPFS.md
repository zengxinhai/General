原文链接：[Learn to securely share files on the blockchain with IPFS!](https://medium.com/@mycoralhealth/learn-to-securely-share-files-on-the-blockchain-with-ipfs-219ee47df54c)
![IPFS with blockchain](https://upload-images.jianshu.io/upload_images/11213662-dc0f9c7830903e65.PNG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**在开始阅读，建议你先阅读我们之前发的一篇文章:
[“Code your own blockchain in less than 200 lines of Go!”](https://medium.com/@mycoralhealth/code-your-own-blockchain-in-less-than-200-lines-of-go-e296282bcffc)**

最近，越来越多的人开始对区块链产生兴趣。虽然大多数关注点被放在加密货币与各种ICO上面，但区块链技术本身也同样令人兴奋。区块链构建了一种民主化的信任与验证协议，已经颠覆了传统银行模式，并且正在对医疗，理财，社交应用等领域产生影响。

然后，从技术上看，区块链也并非没有缺点。目前的PoW(Proof of work)共识机制, 使得交易处理速度十分缓慢，以至于在某些情况下变得几乎没用。风靡一时的加密猫也一度让整个以太坊网络陷入瘫痪。

从区块链的现状来看，在链上存储大量的数据不是一个好的选择。既然区块链只能处理少量字符与文本，记录收付款情况，那我们怎么能在链上直接存储一些较大的文件或者图片之类的数据呢？难道区块链真的只能局限于记录这种小微数据量的应用?

## 引入IPFS
IPFS全称为Interplanet File System，中文可以叫做星际文件系统，由Protocol Labs主导开发。它是目前最有希望能被用于解决这个问题的方案。IPFS是一种点对点的传输协议，每个节点都存储一系列通过hash索引的文件。当某个客户端需要访问这些文件的时候，只需要通过一个巧妙封装过的抽象层，传入文件的hash值。IPFS会通过这个hash值，从活跃的节点当中找到对应的文件，并返回文件内容给客户端。

你可以把IPFS想象成类似我们熟悉的BT下载协议。它是一种去中心化的文件存储与索引方式，通过hash索引，你可以更自如地管理与访问文件，同时提供更加强大的可编程性。

下图简单的表述了IPFS的工作流程:

 ![IPFS上传流程](https://upload-images.jianshu.io/upload_images/11213662-e2105e8441314db0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

1. John打算上传一份PDF文档到IPFS

2. 他首先把PDF文件放到电脑工作区

3. 然后，使用IPFS相关命令添加这个文件，并且得到了文件的hash值。(IPFS的hash值总是以Qm开头，比较好认）

4. 上面动作结束后，这个PDF文件就可以在IPFS上面被访问了。

现在，John打算把这个PDF通过IPFS分享给他的同事Mary。他只需要将第3步得到的hash值告诉Mary，然后Mary就能按图索骥，从IPFS上面下载这份文件。整个过程还挺酷的！
![IPFS下载流程](https://upload-images.jianshu.io/upload_images/11213662-e74369246f0cec82.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 安全漏洞
实际上，这里有一个安全漏洞。任何得到这份PDF hash值的人，都可以轻松从IPFS上下载它。对于带有敏感信息的文件并不适合这样直接分享。因此，当我们需要在IPFS上共享一些敏感文件时，就需要预先对这些文件做一些处理。


## 引入不对称加密
幸运的是，我们有现成的工具能够很好的配合IPFS来安全的共享文件。不对称加密技术能够让我们用文件接收方的公钥加密文件，之后接收方从IPFS下载文件之后，再用私钥解密即可。作恶方就算从IPFS上取得这个文件，也不能做任何事情，因为无法解密其内容。在这个教程中，我们将采用**GPG**不对称加密算法。

让我们重新设一下前面的工作流程，这次引入加密和解密的过程:
![引入加解密后的IPFS文件共享流程](https://upload-images.jianshu.io/upload_images/11213662-6275c2823e514d55.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

1. John打算上传一份PDF到IPFS，但只打算给Mary一个人看。

2. 他将PDF放入电脑的工作区，然后用Mary的公钥对其进行加密。

3. 然后，使用IPFS相关命令添加这个加密后的文件，并且得到了加密文件的hash值。

4. 上面动作结束后，这个加密过的文件就可以在IPFS上面被访问了。

5. Mary得知hash值之后，可以从IPFS上下载，并用她的秘钥解密得到原PDF文件。

6. 任何企图作恶的一方，由于没有Mary的密钥，所以他们无法解密这个文件，从而保证了文件在IPFS上面的安全共享。

## 区块链
讲到现在，那么区块链在这个当中起什么作用呢？在开始前，我们鼓励你去阅读一下我们一个很受欢迎的帖子：[Code your own blockchain in less than 200 lines of Go!](https://medium.com/@mycoralhealth/learn-to-securely-share-files-on-the-blockchain-with-ipfs-219ee47df54c)

下面这张图很重要：
![引自 "Code your own blockchain in less than 200 lines of Go"](https://upload-images.jianshu.io/upload_images/11213662-3b656d54f5ad9efa.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

注意到每个区块中BPM字段，这样的简单字段才是区块链目前能够应付的。这也是为什么加密货币能够很好的在区块链上运作。因为，只要需要记录付款地址，收款地址，转账的比特币(以太坊等）数量，这样简单的字段。由于区块链的链式结构，假如我们把大量文件和数据存放在链上，进行完整性验证的时候，将会是一场十分恐怖的噩梦。

然而，当我们把IPFS和区块链结合在一起的时候，它们就变得十分强大。实际上，我们只在区块链上存储文件的hash值，就像BPM字段那样！这是一个不错的想法。我们在保证区块链上数据简单性的同时，又利用到了IPFS去中心化的文件存储！充分利用了区块链和IPFS的优势。然后，再加上不对称加密技术(GPG)，我们现在有了一套在区块链上优雅地存储，共享大量数据和文件的方法。
![修改后的区块链示意图](https://upload-images.jianshu.io/upload_images/11213662-b40050e46272a589.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在实际应用中，每个区块里存储的可能是健康数据或者实验室数据的hash值。当我们得到一个新的实验结果，我们可以将加密后的实验结果上传到IPFS，在新建的区块内存储相应的hash值即可。

## 说了这么多，看看具体怎么做吧！
本教程包含的内容：
- 配置GPG

- 搭建IPFS

- 用公钥加密文件

- 上传加密文件至IPFS

- 从IPFS下载加密文件，然后确认只有私钥拥有者才能解密内容

#### 需要做的准备

- 一台备用电脑或者虚拟机也行。这台备用电脑就是你的文件接收方。

- 一个测试文件。这个可以自己随意定，PDF文档，txt文件都行。

好了，下面开始！

### 配置GPG

在两台电脑上都安装GPG，[下载链接](http://gnupg.org/download)。如果是Mac的话，直接用```brew install gnupg```命令安装。

用下面的命令，在两台电脑上分别生成key:

```gpg --gen-key```

之后按照提示，输入```name```, ```email``` 然后是密码，确保记住这个密码。

在第二台电脑上导出公钥：

```gpg --export --armor email > pubkey.asc```

把上面命令中的email替换成你配置GPG时填入的```email```地址，运行即可。拷贝```pubkey.asc```文件到你的第一台电脑上。最好用U盘，而不要用电子邮件这样的常规网络传输方式。

拷贝成功后，在你第一台电脑上运行:

```gpg --import pubkey.asc```

这样就导入了第二台电脑的公钥。可以用下面的命令检查是否导入成功:

```gpg --list-keys```

在命令输出结果中，你应该能看到第二台电脑的```name``` 和 ```email```。

都做好之后，GPG的配置就完成了，继续看看IPFS。

### 搭建IPFS

根据[IPFS官方教程](https://ipfs.io/docs/install)，在两台电脑上都下载安装。

安装成功之后，执行：

```ipfs init```

初始化结束之后，再运行: 

```ipfs daemon```

启动ipfs进程。

都成功之后，IPFS搭建就结束了。

### 用公钥加密文件

这里我的测试文件是一个名为 myriad.pdf 的文档，我们用第二台电脑的公钥对其进行加密：

```gpg --encrypt --recipient "Cory Health" myriad.pdf```

*需要注意的是，文件名需要根据你实际的测试文件名做更改，“Cory Health”替换为你第二台电脑公钥的名称。*

加密成功之后，同目录下生成一个后缀名为```.gpg```的文件，只有在你第二台电脑上才能解密并查看这个文件，你可以尝试将它发送给你的朋友，测试是否能打开，就算他们把文件名改回```myriad.pdf```，也无法查看pdf的内容。

现在有了这个加密的文件，我们可以把它上传到IPFS！

### 上传加密文件至IPFS

在我们第一台电脑上运行：

```ipfs add myriad.pdf.gpg```

命令成功之后，会返回一个 Qm开头的hash值，你可以将这个hash值分享给你的朋友，或是任何人，他们就能通过IPFS下载到对应的文件。

为了确保我们上传成功了，我们可以运行:

```ipfs pin ls```

返回结果里面，应该包含刚才的hash值。

### 从IPFS下载加密文件

记住，我们现在是用第二台电脑代表一个接收方，你甚至可以叫你的朋友操作第二台电脑！
在第二台电脑上运行:

```ipfs get hashValue```

把hashValue替换成上一步得到的以Qm开头的hash值，运行并等待下载。

运行结束之后，加密文件就被下载到了你第二台电脑上了。

### 解密文件

在第二台电脑运行:

```gpg --decrypt encryptFile > myriad.pdf```

这个```myriad.pdf```就是解密后的文件，可以直接查看其内容，验证是否解密成功。

哇喔！到这里我已经成功通过IPFS下载，并解密了我们的文件。用这个方式，我们就可以防止其他人查看我们放在IPFS上的文件内容了！

## 总结与展望

现在可以放松庆祝一下了！我们刚才掌握了一个十分强大的方法，它能够解决目前区块链技术的一些关键问题。

回顾一下我们都学到些什么：

- 认识到区块链在数据和文件存储方面的短板

- IPFS的配置和使用

- 利用GPG加密敏感数据，并存储在IPFS

- 理解了IPFS的去中心化文件系统，并且知道如何结合区块链去管理这些hash值。同时发挥了区块链和IPFS系统的优点。

之后，你可以根据自己的实际情况去使用你在这里学到的东西。值得注意的是，如果你的文件在IPFS节点上不是很受欢迎的话，那么你停掉自己的节点之后，很可能没有其他的节点去保管你的文件。从而，你的文件可能会从IPFS上消失。解决的办法就是，你可以利用云服务搭建一个IPFS节点，来保管你的文件，直到你确定你的文件足够受欢迎。

还有，你可以随时告诉我们，你期望之后的文章是关于什么方面的！我们很乐意做一些区块链相关的技术教程。通过[Telegram](https://t.me/joinchat/FX6A7UThIZ1WOUNirDS_Ew)或者[Twitter](https://twitter.com/myCoralHealth)可以联系到我们！欢迎沟通交流！
