# Commit Message 格式

目前规范使用较多的是 Angular 团队的规范, 继而衍生了 Conventional Commits specification. 很多工具也是基于此规范, 它的 message 格式如下:

```md
<type>(<scope>): <subject>
<BLANK LINE>

<body>
<BLANK LINE>
<footer>
```

我们通过 git commit 命令带出的 vim 界面填写的最终结果应该类似如上这个结构, 大致分为三个部分(使用空行分割):

- 标题行: 必填, 描述主要修改类型和内容
- 主题内容: 描述为什么修改, 做了什么样的修改, 以及开发的思路等等
- 页脚注释: 放 Breaking Changes 或 Closed Issues

分别由如下部分构成:

- type: commit 的类型

1. feat: 新增功能
2. fix: 修改问题
3. refactor: 代码重构
4. docs: 文档修改
5. style: 代码格式修改, 注意不是 css 修改
6. test: 测试用例修改
7. chore: 其他修改, 比如构建流程, 依赖管理.

- scope: commit 影响的范围, 比如: route, component, utils, build...
- subject: commit 的概述, 建议符合 50/72 formatting
- body: commit 具体修改内容, 可以分为多行, 建议符合 50/72 formatting
- footer: 一些备注, 通常是 BREAKING CHANGE 或修复的 bug 的链接.

这样一个符合规范的 commit message, 就好像是一份邮件

> 以上内容摘抄于
> 作者：阿里南京技术专刊
> 链接：<https://juejin.im/post/5afc5242f265da0b7f44bee4>
> 来源：掘金
