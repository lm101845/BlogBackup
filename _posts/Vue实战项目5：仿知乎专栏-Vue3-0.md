---
title: Vue实战项目5：仿知乎专栏(Vue3.0)
date: 2021-05-02 13:48:45
tags: 前端实战
categories: 前端实战 
---

(注1：该项目的相对应文档：[从零到一开发到上线 高仿知乎专栏](http://docs.vikingship.xyz/))

# TypeScript介绍

##  编程语言的类型

![](Vue实战项目5：仿知乎专栏-Vue3-0/01.png)

## TypeScript究竟是什么

![](Vue实战项目5：仿知乎专栏-Vue3-0/02.png)

## TypeScript全套相关配置

`tsconfig.json`

~~~javascript
{
  "include": ["src", "demo"],
  "compilerOptions": {
    "module": "commonjs",
    "noImplicitReturns": true,
    "noUnusedLocals": true,
    "esModuleInterop": true,
    "target": "esnext",
    "strict": true,
    "outDir": "app",
    "declaration": true,
    "sourceMap": true
  }
}
~~~

`jest.config.js`

~~~javascript
module.exports = {
  roots: ['<rootDir>/src'],
  transform: {
    '^.+\\.tsx?$': 'ts-jest',
  },
  testPathIgnorePatterns: ['/node_moudles/', './src/utils/test.ts'],
}
~~~

`babel.config.js`

~~~javascript
module.exports = {
  presets: ['@babel/typescript'],
  plugins: [
    '@babel/plugin-transform-modules-commonjs',
    '@babel/proposal-class-properties',
    '@babel/proposal-object-rest-spread',
  ],
}
~~~

## 小贴士

* TypeScript即使编译报错了，还是会生成编译后的结果的，我们仍然可以使用编译后的文件的。

* undefined和null是所有类型的子类型，  举个例子，undefined类型的变量可以赋值给number类型的变量。

![](Vue实战项目5：仿知乎专栏-Vue3-0/03.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/04.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/05.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/06.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/07.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/08.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/09.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/10.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/11.png)

![](Vue实战项目5：仿知乎专栏-Vue3-0/12.png)