# XFYun TTS

[![js-standard-style](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://github.com/feross/standard)
[![action][ci-image]][ci-url]
[![license][license-image]][repository-url]
[![NPM version][npm-image]][npm-url]
[![npm download][download-image]][download-url]

[ci-image]: https://img.shields.io/github/workflow/status/funnyzak/xfyun-tts/Node.js%20CI
[ci-url]: https://github.com/funnyzak/xfyun-tts/actions
[license-image]: https://img.shields.io/github/license/funnyzak/xfyun-tts.svg?style=flat-square
[repository-url]: https://github.com/funnyzak/xfyun-tts
[npm-image]: https://img.shields.io/npm/v/@funnyzak/xfyun-tts.svg?style=flat-square
[npm-url]: https://npmjs.org/package/@funnyzak/xfyun-tts
[download-image]: https://img.shields.io/npm/dm/@funnyzak/xfyun-tts.svg?style=flat-square
[download-url]: https://npmjs.org/package/@funnyzak/xfyun-tts

讯飞云语音合成 Node 模块。

## 开始

from [npm](https://github.com/npm/npm)

    $ npm install @funnyzak/xfyun-tts

## 用例

```js
const { XFYunTTS } = require('@funnyzak/xfyun-tts');
const path = require('path');

!(async () => {
  const _xfyTTS = new XFYunTTS(
    {
      appId: 'appid',
      apiSecret: 'apisecret',
      apiKey: 'apikey',
      host: 'tts-api.xfyun.cn',
      uri: '/v2/tts',
      hostUrl: 'wss://tts-api.xfyun.cn/v2/tts'
    },
    path.join(process.cwd(), new Date().getTime().toString()) /** optional **/
  );

  // send
  console.log((await _xfyTTS.send('你好')).);

  // more ...
})();
```

了解更多 [nls define](lib/nls.d.ts).

## Author

| [![twitter/funnyzak](https://s.gravatar.com/avatar/c2437e240644b1317a4a356c6d6253ee?s=70)](https://twitter.com/funnyzak 'Follow @funnyzak on Twitter') |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [funnyzak](https://yycc.me/)                                                                                                                           |

## 参考

- [文本语音合成文档](https://www.xfyun.cn/doc/tts/online_tts/API.html)
- [错误慢参考解决](https://www.xfyun.cn/document/error-code)

## License

Apache-2.0 License © 2021 [funnyzak](https://github.com/funnyzak)
