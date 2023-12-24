こちらは「HayabusaTrip」のフロントエンドのリポジトリになります。バックエンドのリポジトリは[こちら](https://github.com/keynyaan/hayabusatrip-backend)です。

# EAT FISH / おいしいお魚情報共有サービス

![service-image](https://github.com/Karukan0814/EatFish_All/blob/master/assets/EatFishImg.png)
![EatFish_Backend](https://img.shields.io/badge/Backend-Node.js%20%3E%3D16.13.0%20%2F%20TypeScript%205.2.2-brightgreen)
![EatFish_Frontend](https://img.shields.io/badge/Frontend-TypeScript%3A%205.2.2%20%2F%20React%2018.2.0%20%2F%20Next.js%2013.2.4-blue)
[![Docker](https://img.shields.io/badge/Docker-gray?logo=Docker&logoColor=2496ED)](https://www.docker.com)
[![Firebase](https://img.shields.io/badge/Firebase-gray?logo=Firebase&logoColor=FFCA28)](https://firebase.google.com)
[![Thanks](https://img.shields.io/badge/Thank%20you-for%20visiting-00aab9)](https://www.eatfish.com)

## サービス概要

EAT FISH はおいしいお魚ライフに役立つレシピ記事や魚屋・お取り寄せ先情報を、季節ごとのお魚別に整理したデータベースサービスです。

ユーザーは食べたいお魚の情報を検索することができます。

### ▼ サービス URL

https://eatfish-psi.vercel.app/

レスポンシブ対応済のため、PC でもスマートフォンでも快適にご利用いただけます。

### ▼ 紹介記事(Qiita)

TODO 　紹介記事書く

開発背景や、サービスのリリースまでに勉強したことなどをまとめています。

### ▼ 開発者 Twitter

TODO 　開発者アカウント作成

何かあれば、こちらまでお気軽にご連絡ください。

## メイン機能の使い方

<br>

## 主な機能

### コア機能（カテゴリ絞り込み・ブックマーク+α）

| カテゴリ絞り込み                                                                                                                    | ブックマーク・いいね                                                                                                                | コメント                                                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Image from Gyazo](https://i.gyazo.com/f43ddd0aca232a7f5df0a193f51a73c0.gif)](https://gyazo.com/f43ddd0aca232a7f5df0a193f51a73c0) | [![Image from Gyazo](https://i.gyazo.com/8910bd2f80c2bf9e5f65e2cb351c3a38.gif)](https://gyazo.com/8910bd2f80c2bf9e5f65e2cb351c3a38) | [![Image from Gyazo](https://i.gyazo.com/001e2dd07b9512f77945cbdcfa0e25a4.gif)](https://gyazo.com/001e2dd07b9512f77945cbdcfa0e25a4)                        |
| カテゴリアイコンをタップすることで、そのカテゴリに紐付いた記事一覧が表示されます。                                                  | 記事右下の各種ボタンをタップすることで、ブックマークといいねができます （**ログインユーザー限定**）                                 | コメントボタンをタップすると、モーダルが立ち上がり各記事についたコメントを閲覧できたり、コメントの投稿・編集・削除ができます。（**ログインユーザー限定**） |

<br>

### ユーザー機能

| ログイン                                                                                                                            | マイページ上で記事を管理                                                                                                            |
| :---------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| [![Image from Gyazo](https://i.gyazo.com/670f1953ffa6efede6bec8c87b1af81a.png)](https://gyazo.com/670f1953ffa6efede6bec8c87b1af81a) | [![Image from Gyazo](https://i.gyazo.com/a3183825d24f38257c3f0b9d2e69fbfa.gif)](https://gyazo.com/a3183825d24f38257c3f0b9d2e69fbfa) |
| ログインボタンを押すと、モーダルが立ち上がり Google ログインが可能になります。                                                      | マイページ上でブックマークやいいねした記事を管理することができます。                                                                |

<br>

## 使用技術一覧

**バックエンド:** Node.js 　>=16.13.0 / TypeScript 5.2.2

- フレームワーク: Express.js (^4.18.2)
- データベースクライアント: Prisma (^5.5.2)
- テストフレームワーク: Jest (^29.7.0)
- HTTP クライアント: Axios (^1.6.1)
- セキュリティ: Helmet (^7.1.0), JSON Web Tokens (jsonwebtoken) (^9.0.2)
- ロギング: Morgan (^1.10.0)
- その他依存関係: Cheerio (^1.0.0-rc.12), CORS (^2.8.5), dotenv (^16.3.1), express-validator (^7.0.1), iconv-lite (^0.6.3)

**フロントエンド:** TypeScript: 5.2.2 / React 18.2.0 / Next.js 13.2.4

- スタイリング: @emotion/react 11.11.1, @emotion/styled 11.11.0, @mui/material 5.14.16
- アイコン: @mui/icons-material 5.14.16
- HTTP クライアント: axios 1.6.0
- 状態管理: jotai 2.5.0
- 認証: firebase 10.5.2-authentification,jsonwebtoken 9.0.2
- データ保存: firebase 10.5.2-storage
- フォーム管理: react-hook-form 7.47.0
- テストフレームワーク: @testing-library/react 14.1.2, jest 29.7.0

リント / コード解析: eslint 8.52.0, eslint-config-next 14.0.1

**インフラ:**
Supabase / render / Vercel

**CI / CD:** GitHub Actions

**テスト環境構築:** Docker

**認証:** Firebase Authentication 　/ jsonwebtoken

## 主要対応一覧

### ユーザー向け

#### 機能

- Google アカウントを利用したユーザー登録 / ログイン機能
- ユーザー情報変更機能
- 退会機能
- 旅行プランの取得 / 作成 / 更新 / 削除機能
- 旅行プランの検索機能
- 旅行プランの公開 / 非公開機能
- 旅行スポットの取得 / 作成 / 更新 / 削除機能
- Twitter シェア機能
- ページネーション機能
- 画像の取得 / アップロード機能

#### 画面

- トースト表示
- ローディング画面
- モーダル画面(各画面の詳細は[下記](#screen-transition-diagram)の画面遷移図参照)
- 404 / 500 エラーのカスタム画面
- レスポンシブデザイン

#### テスト / セキュリティ

- クロスブラウザテスト

  - PC
    - Windows10 / 11: Google Chrome / Firefox / Microsoft Edge
    - Mac: Google Chrome / Firefox / Safari
  - スマートフォン
    - Android: Google Chrome
    - iOS: Safari

- Codecov によるコードカバレッジの分析と可視化
- 脆弱性対応(Dependabot Alerts / Code Scanning Alerts / GitGuardian)

## インフラ構成図

![infrastructure-diagram](https://github.com/Karukan0814/EatFish_All/blob/master/assets/infrastructure.drawio)

## ER 図

![er-diagram](https://github.com/Karukan0814/EatFish_All/blob/master/assets/Supbase%20Schema.png)
<a id="screen-transition-diagram"></a>

## 画面遷移図

[Figma\_画面遷移図](https://www.figma.com/file/1OgxVeGaDw9riHGzxyGoLG/%E7%94%BB%E9%9D%A2%E9%81%B7%E7%A7%BB%E5%9B%B3_HayabusaTrip?type=design&node-id=0-1&mode=design)
