# 广东工业大学课程攻略共享计划

## 介绍
这里是广东工业大学课程攻略共享计划   
[Github](https://github.com/gdutday/gdut-lib): https://github.com/gdutday/gdut-lib  
[Gitee](https://gitee.com/gdutday/gdut-lib): https://gitee.com/gdutday/gdut-lib   (推荐)

## gdutday小程序端下载源
[Gitee](https://gitee.com/gdutday/gdut-lib): https://gitee.com/gdutday/gdut-lib  

## 接口使用
我们提供一个可以外部调用获取目录，下载文件的简明教程。

1. 获取根目录下的文件文件夹
url: https://gitee.com/api/v5/repos/gdutday/gdut-lib/git/trees/master  
提交方式: GET  
返回值: 
```json
{
	"sha":"key"
	"url":"url"
	"tree":[
		{
			"path":"数据结构",
			"mode":"040000",
			"type":"tree",
			"sha":"d4efe9b0c0b9fbaf27c497dd9c614433126af02a",
			"url":"url"
		}
		{
			"path":"README.md",
            "mode":"100644",
            "type":"blob",
            "sha":"79c35504709fd527381be252128e470ef96e9dc9",
            "size":675,
            "url":"url"
        }
	]
}
```
上面讲述了大体的返回值，而我们需要用到的事 tree 中的元素。  
首先对tree中的属性进行简要说明：  
1. path: 文件/文件夹名
1. type: 类型，文件夹为tree，文件为blob
1. tree.url: (指type为tree的url) 获取这个文件夹下的目录信息
1. blob.size: 文件大小 Bit  

所以我们需要用到的就是这些信息，这边简要说明下如何实现获取文件目录与下载  
1. 如果type为tree，那么他对应点击后应该是获取其下的文件目录，这里的点击url则对应tree的url  
1. 如果type为blob，则点击他后为下载文件，这里的url应该为  https://gdutday.gitee.io/gdut-lib + (文件所在的路径) + (文件名)，举个例子，根目录即主目录(文件所在路径为 / )下的README.md(文件名)的下载路径应该为https://gdutday.gitee.io/gdut-lib/README.md 。"/数据结构/试卷/数据结构重点 - 用于合并.docx" 则为 https://gdutday.gitee.io/gdut-lib/数据结构/试卷/数据结构重点 - 用于合并.docx     点击后将直接下载

以上是简明的调用教程，具体如何实现，就看各位的使用了。

## 资料来源
1. 各位同学的收集
1. https://github.com/brenner8023/gdut-course

## 版权免责声明
1. 资料为市面收集而来，如遇到版权问题，请联系邮箱 cerbur@qq.com ，我们会主动删除有版权纠纷的文件。