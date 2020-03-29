# 广东工业大学课程攻略共享计划

## 介绍
这里是广东工业大学课程攻略共享计划 
[Github](https://github.com/gdutday/gdut-lib): https://github.com/gdutday/gdut-lib  
[Gitee](https://gitee.com/gdutday/gdut-lib): https://gitee.com/gdutday/gdut-lib   (推荐)

## gdutday小程序端下载源
[Gitee]https://gitee.com/gdutday/gdut-lib): https://gitee.com/gdutday/gdut-lib  

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
	]
}
```


## 资料来源
1. 各位同学的收集
1. https://github.com/brenner8023/gdut-course

## 版权免责声明
1. 资料为市面收集而来，如遇到版权问题，请联系邮箱 cerbur@qq.com ，我们会主动删除有版权纠纷的文件。