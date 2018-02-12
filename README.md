---
Title: Tech Docs
Description: Tech Docs collects all documents written by Joe.
ShowOnHome: false
---
在线查阅请访问 [旧书 Tech. Docs 官网](http://tech.jiu-shu.com)
# 文档注意事项
- 文件名不要出现‘.’
- 尽量使用英文文件夹；尽量使用英文文件名
- 文件夹和文件名避免使用空格，可以使用-作为连接符

# GIT相关问题应对
在linux上clone后，如果通过了chmod来修改文件夹及子目录的权限后，所有目录的文件git状态变成modified； 如果尝试用 `git diff` 查看会发现类似如下信息：
```
...
diff --git a/Dev-Ops/Centos-Common-Commands.md b/Dev-Ops/Centos-Common-Commands.md
old mode 100644
new mode 10075
...
```
以上是权限模型改变导致的，可以通过设置 `git config core.filemode false` 绕过这个问题：

# GITHUB Webhooks 使用
通过github的webhooks，可以对github上的事件进行监听并且发送post请求。 可以在我们的web server端来接受post请求做出相应的操作。
