# GenericAgent 拆解课

把 [GenericAgent](https://github.com/lsdefine/GenericAgent)（一个约 3000 行的自进化智能体框架）拆成一门 **交互式中文课程**，面向「不懂代码但想看懂底层、想更好地指挥 AI」的人。

一个**零依赖、纯静态**的单页网站：滚动式分章、代码与大白话左右对照、数据流动画、组件群聊、术语悬浮释义、即时小测验。打开浏览器即可学，无需任何安装。

## 在线访问

> 部署到 GitHub Pages 后，链接会出现在这里。

## 本地打开

直接双击 `index.html`，或：

```bash
# 任选其一起个本地服务器
python3 -m http.server 8000
# 然后浏览器访问 http://localhost:8000
```

## 课程大纲

| 章 | 标题 | 讲什么 |
|---|---|---|
| 01 | 你扔一句话，它接管整台电脑 | GA 是什么 + 追踪一句话如何变成一串动作 |
| 02 | 100 行的心跳 | 把核心循环比作回合制游戏，逐行读 |
| 03 | 9 件原子工具 | 乐高式工具组合、命名约定分发、两道隐形护栏 |
| 04 | 分层记忆 | 每回合擦白板却不失忆 · 何时读写 · 省钱细节 |
| 05 | 自我进化 | 把成功经验「结晶」成技能，越用越强 |

## 改内容 & 重新构建

课程是「拆件式」结构，内容只在 `modules/*.html` 里：

```bash
# 改完任意模块后，重新拼装 index.html
bash build.sh
```

`styles.css` / `main.js` 是预置的交互引擎，一般无需改动。

## 致谢

- 课程对象：[lsdefine/GenericAgent](https://github.com/lsdefine/GenericAgent)
- 生成方式：Claude Code 的 `codebase-to-course` 技能（[zarazhangrui/codebase-to-course](https://github.com/zarazhangrui/codebase-to-course)）
