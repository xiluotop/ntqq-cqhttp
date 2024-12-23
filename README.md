# ntqq-cqhttp jsbot node.js API更新记录

  文档可参考官方文档，基本以官方数据以及 API 命名方法
  更新内容 api 示例使用方法可参考 test.js 代码

  基本使用方式：

  ```javascript
  // 引入平台 SDK
  const BotSDK = require('./go-cqhttp-jsbot.js').BotSDK
  // 实例化一个平台，框架地址，反向上报端口
  const botSDK = new BotSDK('localhost', 8888);
  // 创建一个监听 bot 对象（已挂载至框架内的 qq），正向端口
  let bot = botSDK.createBot('123456789', 52566);
  // -------------
  ... 可在 test.js 里参照 api 示例使用 bot.xxx 形式注册或调用相关指令功能。
  // -------------
  ```

## v1.0.0
  
* 本项目移植自 https://github.com/xiluotop/go-cqhttp-jsbot
* 当前完成如下
  * 封装 bot 操作 api 支持统一事件、私聊、群聊消息监听
  * 支持快速鉴定指定群消息，自定义快捷指令
  * 实现发送私聊，群私聊，群聊
  * 当前仅完成一些常用方法，许多其他事件没有还没有处理好分发，其他请求操作可以根据官方文档使用内置 http 请求完成 post 请求
* 随着 ntqq 的 hook 方法愈加完善安全，基于社区大佬们的成果随缘重新更新一些内容
* 本人代码水平不高，会尽力去完善，有问题或者可以改善的地方还请多多指教

## API 查询

见 <https://llonebot.github.io/zh-CN/develop/api>

## 鸣谢

- [NapCatQQ](https://github.com/NapNeko/NapCatQQ)
- [LiteLoaderQQNT](https://liteloaderqqnt.github.io/guide/install.html)
- [Chronocat](https://github.com/chrononeko/chronocat)
- [koishi-plugin-adapter-onebot](https://github.com/koishijs/koishi-plugin-adapter-onebot)
- [silk-wasm](https://github.com/idranme/silk-wasm)
