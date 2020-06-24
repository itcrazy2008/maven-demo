# 将代码部署到maven中央仓库示例

* https://blog.csdn.net/a979331856/article/details/89498455
* 关键的步骤如下：
  * sonatype申请账号
  * 在JIRA上创建 Issue,等待审核
  * 下载 Gpg4win 软件，处理GPG信息，生成并发布公钥（注意公钥ID 可能是16位的比较准，8位的对吗？）
  * 新建项目，注意pom.xml文件，非常严格，下载maven的各插件
  * 配置本地的全局的settings.xml，和pom.xml中的id对应起来
  * 提交项目代码到oss
  * 然后在oss上close和release，成功后过2个小时，就可以在maven中央仓库查询到自己提交的代码并通过dependencies引用
  * 通知工作人员关闭Issue