# lighthouse-ci × Nuxt3

## 何を実現したいか
* CIの中でCore Web Vitalsのパフォーマンスを調査したい

## 行ったこと
* lighthouse-ciを用いてパフォーマンスを計測
* 今回はCore Web Vitalsのみに着目のため他の指標は何もしない

## 環境
* [Nuxt.js](https://nuxt.com/) v3.x
* [lighthouse-ci](https://github.com/GoogleChrome/lighthouse-ci) v0.12.x

## 確認コマンド
### ページを計測する
```
$ npx lhci autorun
```

## 現在設定の指標(Google公式のpoorを閾値として設定)
* Largest Contentful Paint（LCP）
  * 4000ミリ秒以上でエラー
* First Input Delay（FID）
  * 300ミリ秒以上でエラー
* Cumulative Layout Shift（CLS）
  * 0.25以上でエラー

## 参考
* [Google - Core Web Vitals の指標](https://developers.google.com/search/docs/appearance/core-web-vitals?hl=ja)
* [lighthouse-ci - 設定ファイル](https://github.com/GoogleChrome/lighthouse-ci/blob/main/docs/configuration.md)
* [lighthouse - 設定キー](https://github.com/GoogleChrome/lighthouse/blob/v5.5.0/lighthouse-core/config/default-config.js)
