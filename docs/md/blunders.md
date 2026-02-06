# 糗事集锦

## 写在前面
这里是糗事集锦，主要记录了开发过程中的一些~~趣逝~~趣事。  
我不会把它写得太正式，所以它的语言风格和其他的差别很大。  
另外，本文中的**不出汗**指的是[Bychuhan](https://github.com/Bychuhan)。  

## 提交撤回这一块。
不出汗某次提交时手滑提交错了文件，想着在本地撤掉，结果撤回时不小心多撤了几个有效提交。  
慌乱中看到 VSCode 源代码管理里那个醒目的提交按钮，不假思索就点了下去。  
然后就触发了自动合并。  

不知道是 VSCode 还是 Git 干的，总之它贴心地为不出汗生成了一个空白的合并提交。  
大概是 `Merge branch 啥啥啥 into 啥啥啥` 之类的。  

不出汗生气了。竟敢不遵守提交信息规范。  
不出汗试图撤回这个提交，结果把旁边正常的提交给误伤了。  

情急之下，不出汗开始用 Git 强行删除提交。  
一通操作猛如虎，不小心执行了拉取。  
云端代码把本地代码覆盖得一干二净，还没来得及提交的新代码也没了。  

不出汗位居了。突然想起VSCode的时间线功能，点开找回了丢失的代码。  
然后这个B发现源代码管理的分支视图惨不忍睹。  
不错的视图。本地和云端相互呼应。线图缠绕，历史错综。即使是我，也感到忍俊不禁。  

最后不出汗创建了新分支，把云端提交记录移植过去，删除了原来那个错综复杂的分支。  
一通操作花了得有一个小时。哈哈。

::: warning
上文中的内容是根据记忆复原的，可能和事实有偏差。
:::

## 论为什么文档要和主仓库分家
虽然这个和上面的比起来也不算是糗事了。但是我还是想写。

不出汗在主仓库(RePyPhiRenderer)的docs/目录下用Vitepress给项目写文档。  
不出汗原本想部署在 [/pypr-docs/](https://bychuhan.github.io/pypr-docs/) 下，结果提交之后，由于Github Pages的限制，文档被部署到 [/RePyPhiRenderer/](https://bychuhan.github.io/RePyPhiRenderer/) 了。  
看哭了。  

不出汗临时提交删掉了文档相关的文件 ([82f702a](https://github.com/Bychuhan/RePyPhiRenderer/commit/82f702a29b5e838a40d31144ba6cd65ccc28c971))，并撤掉了页面。  

另外不出汗在这个提交发表了[评论](https://github.com/Bychuhan/RePyPhiRenderer/commit/82f702a29b5e838a40d31144ba6cd65ccc28c971#commitcomment-176495674)，并获得了来自[K0nGbawa](https://github.com/K0nGbawa)的一个[👀]  
哦对还有就是不出汗一开始把评论里的"**预期**"打成"**预取**"了。  

最后无奈，不出汗只得给文档单独建了 [pypr-docs](https://github.com/Bychuhan/pypr-docs) 仓库。