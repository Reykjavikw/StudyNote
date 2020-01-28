**PyCharm使用笔记**

[TOC]

### 各类设置

#### · 导入项目

​	`File` ->`Settings`->`Project:name`->`Project interpreter`->`add`->`New environment/Exiting environment`



------



### 使用时碰见的问题

#### · PyCharm报错：Cannot save settings : Please specify a different SDK name

​	**原因**：PyCharm中存在相同名字的虚拟环境变量

​	**本次出错具体原因**：导入项目时出错

​	**解决方法**：`File` ->`Settings`->`Project:name`->`Project interpreter`->`Show all`-> 在弹出的对话框里删除标红选项(相同虚拟环境名字的虚拟环境)