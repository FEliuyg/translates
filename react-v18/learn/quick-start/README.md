# 快速开始

欢迎来到 React 文档！这个页面将介绍 80% 的你基本每天都会用得到的 React 概念。

你将会学到什么

- 如何创建和嵌套组件
- 如何添加标记和样式
- 如何显示数据
- 如何条件渲染和渲染列表
- 如何响应事件和更新视图
- 如何在组件之间共享数据

## 创建和嵌套组件

React 应用是由组件所构成的。组件是拥有自己的内部逻辑和样式的一部分用户界面（UI)。一个组件可以小到一个按钮，大到一个完整的页面。

React 组件是 JavaScript 函数，返回标签。

```jsx
function MyButton() {
  return <button>I'm a button</button>;
}
```

现在你已经声明了 `MyButton`，你可以将它嵌入其他的组件：

```jsx
export default function MyApp() {
  return (
    <div>
      <h1>Welcome to my app</h1>
      <MyButton />
    </div>
  );
}
```

注意 `MyButton` 以大小字母开头。这规则可以让你知道它是一个 React 组件。React 组件的名字必须始终以大写字母开头，HTML 标签必须是小写的。

看一下结果：
[代码实例](https://codesandbox.io/s/4c3fsr?file=%2FApp.js&from-sandpack=true)

`export default` 关键字定义了这个文件的主组件。如果你不熟悉这个语法，[MDN](https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export) 和 [javascript.info](https://javascript.info/import-export) 有很好的介绍。

## 用 JSX 写标签

你在上面看到的标签语法成为 _JSX_ , 大多数的 React 项目都会使用 JSX，因为它简便。所有[推荐的本地开发方式](../installation/README.md) 都开箱即用地支持 JSX。

JSX 比 HTML 还严格，你必须闭合标签，比如 `<br />`。你的组件也不能返回多个 JSX 标签，你必须用个父标签将他们包裹起来，比如 `<div>...</div>` 或者空标签 `<>...</>`:

```jsx
function AboutPage() {
  return (
    <>
      <h1>About</h1>
      <p>
        Hello there.
        <br />
        How do you do?
      </p>
    </>
  );
}
```

如果你有很多 HTML 需要转换成 JSX 语法，你可以用[在线转换工具](https://transform.tools/html-to-jsx)。
