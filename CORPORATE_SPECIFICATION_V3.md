# 株式会社ロクブンノニ 法人Webサイト 完全仕様書 v3.0
## メディア事業中心・全サービス詳細展開版

## 🎯 プロジェクト概要（メディア事業中心版）

### 会社概要
- **会社名**: 株式会社ロクブンノニ
- **英語名**: Rokubunnoni Inc. / 6BUNNO2 Inc.
- **ドメイン**: rokubunnoni.com
- **事業領域**: 
  - **Crypto Times**: Web3専門メディア運営（主力事業・2018年〜）
  - **Crypto Times Ventures**: Web3投資事業
  - **コンサルティング**: 戦略策定・トークンエコノミクス設計
  - **開発サービス**: dApp・プロトコル開発
  - **リサーチ**: 市場調査・分析レポート

### 企業ポジション
**「Web3メディアとエコシステム構築の専門企業」**
- 2018年から運営する日本最大級のWeb3専門メディア
- メディアの知見を活かした投資・コンサルティング事業
- データドリブンなアプローチで業界をリード

### ミッション・ビジョン・バリュー（空欄：後ほど追記）

#### Mission（使命）
```
[TODO: 会社の使命を記載]
例：Web3の可能性を投資と事業支援で実現し、次世代デジタル経済を牽引する
```

#### Vision（ビジョン）  
```
[TODO: 目指す未来像を記載]
例：アジア発で世界をリードするWeb3エコシステムを構築し、100社のユニコーン企業を創出する
```

#### Values（価値観）
```
[TODO: 企業の価値観を記載]
例：
- Data-Driven Excellence（データ駆動の卓越性）: 感情ではなく、データに基づく投資判断
- Long-term Partnership（長期パートナーシップ）: 投資先の成功まで伴走するコミットメント
- Ecosystem Building（エコシステム構築）: 単独成功でなく、業界全体の発展を追求
- Transparency & Trust（透明性と信頼）: ステークホルダーへの誠実な情報開示
- Global Perspective（グローバル視点）: ローカルに根ざし、世界に通用する価値創造
```

### ターゲットユーザー（再定義）

#### Primary Target: 投資家・LP（40%）
- **個人投資家**: 富裕層・エンジェル投資家・業界関係者
- **機関投資家**: VCファンド・ファミリーオフィス・年金基金
- **戦略投資家**: 大手企業のCVC・金融機関・政府系ファンド
- **ニーズ**: Web3投資機会・ファンド出資・共同投資

#### Secondary Target: 投資先候補企業（35%）
- **海外Web3企業**: アジア・日本進出を検討中
- **国内Web3企業**: 資金調達・事業拡大サポート
- **起業家・創業チーム**: アイデア段階から成長期まで
- **ニーズ**: 資金調達・戦略支援・事業開発

#### Tertiary Target: 事業パートナー（25%）
- **メディア・PR企業**: 広告・プロモーション連携
- **技術パートナー**: 開発・インフラ提供
- **法的・会計パートナー**: コンプライアンス・税務
- **ニーズ**: 業務提携・協業・知見共有

## 🏗️ 技術アーキテクチャ（更新版）

### フロントエンド
- **フレームワーク**: Next.js 15 (App Router)
- **言語**: TypeScript 5.x
- **スタイリング**: Tailwind CSS 4.x
- **国際化**: next-intl
- **状態管理**: Zustand
- **フォーム**: React Hook Form + Zod
- **アニメーション**: Framer Motion
- **チャート**: Recharts / D3.js（投資データ可視化）

### ナビゲーション・UX
- **レスポンシブメニュー**: ハンバーガーメニュー実装
- **階層構造**: ドロップダウン・メガメニュー対応
- **モバイル最適化**: タッチフレンドリー・スワイプ対応
- **アクセシビリティ**: WCAG 2.1 AA準拠・キーボード操作

### 認証・セキュリティ
- **会員制機能**: NextAuth.js実装
- **LP専用エリア**: パスワード保護・2FA対応
- **投資家認証**: KYC・AML対応検討
- **データ保護**: 暗号化・ログ監視

## 📄 サイト構成（投資事業強化版）

### グローバルナビゲーション（更新）
1. **Home** (/)
2. **About** (/about)
   - Company Overview
   - Mission & Vision & Values
   - Team & Advisors
   - History & Milestones
3. **Media** (/media) ← **★主力事業（Crypto Times）**
   - About Crypto Times
   - Editorial Policy
   - Advertising & Partnership
   - Media Kit
4. **Ventures** (/ventures)
   - Investment Philosophy
   - Portfolio Companies
   - Investment Team
   - For Investors (LP向け)
5. **Services** (/services)
   - Consulting Services
   - Development Services
   - Research & Analytics
6. **Works** (/works)
   - Case Studies
   - Success Stories
   - Client Portfolio
7. **Insights** (/insights)
   - Market Analysis
   - Technical Research
   - Industry Reports
8. **Newsroom** (/newsroom)
   - Press Releases
   - Media Coverage
   - Awards & Recognition
9. **Contact** (/contact)

### レスポンシブナビゲーション仕様

#### デスクトップ（1024px+）
```
Header Layout:
[Logo] [About] [Media ▼] [Ventures ▼] [Services ▼] [Works] [Insights] [Newsroom] [Contact] [言語切替] [お問い合わせ]

Media Dropdown (主力事業):
- About Crypto Times
- Editorial Policy
- Advertising & Partnership
- Media Kit

Ventures Dropdown:
- Investment Philosophy
- Portfolio Companies  
- Investment Team
- For Investors

Services Dropdown:
- Consulting Services
- Development Services
- Research & Analytics
```

#### タブレット（768px-1023px）
```
Header Layout:
[Logo] [メニュー ≡]

ハンバーガーメニュー展開:
- About
- Ventures >
  - Investment Philosophy
  - Portfolio Companies
  - Investment Team
  - For Investors
- Services >
  - Crypto Times
  - Consulting Services
  - Development Services
  - Research & Analytics
- Works
- Insights
- Newsroom
- Contact
- 言語切替
```

#### モバイル（〜767px）
```
Header Layout:
[≡] [Logo] [お問い合わせ]

フルスクリーンメニュー:
[同階層構造、タッチ最適化]
```

## 📋 詳細ページ設計（投資事業特化）

### 1. Ventures (/ventures) - 「投資事業メインページ」

#### Investment Philosophy (/ventures/philosophy)
**投資哲学・戦略の詳細説明**

```
コンテンツ構成:
1. Philosophy Overview
   - 投資理念・思想
   - Web3/ブロックチェーンへの信念
   - 長期的ビジョン

2. Investment Thesis
   - 投資テーマ・セクター
   - 市場機会の分析
   - 独自の投資判断基準

3. Investment Process
   - デューデリジェンス・プロセス
   - 投資委員会の構成
   - 投資実行までのフロー
   - ポストインベストメント支援

4. Value Addition
   - 投資先への付加価値
   - メディア・エコシステム活用
   - 戦略的パートナーシップ
   - 経営支援・メンタリング

5. Investment Criteria
   - 投資対象セクター
   - 投資ステージ（Seed〜Series B）
   - 投資金額レンジ
   - 地域・マーケット

6. Team Philosophy
   - 投資チームの考え方
   - 意思決定プロセス
   - リスク管理方針
```

#### Portfolio Companies (/ventures/portfolio)
**投資先企業の紹介・実績**

```
フィルタリング機能:
- セクター別（DeFi, GameFi, NFT, Infrastructure, etc.）
- ステージ別（Seed, Series A, Series B, etc.）
- 地域別（Japan, Asia, Global）
- 投資年別（2020-2025）
- ステータス別（Active, Exited, IPO）

各投資先情報:
一般公開レベル:
- 企業ロゴ・名称
- 事業概要（100字程度）
- セクター・タグ
- 投資年・ラウンド
- 公式サイトリンク
- 注目ポイント

限定公開レベル（LP向け）:
- 詳細事業説明
- 投資金額・持分比率
- 投資時評価額・現在評価額
- KPI・成長指標
- Exit戦略・IPO予定
- リスク要因

成功事例ハイライト:
- Exit実績（IPO・M&A）
- 評価額成長率
- 代表的投資先の詳細
- 投資リターン（IRR・MOIC）
```

#### Investment Team (/ventures/team)
**投資チーム・アドバイザー紹介**

```
チーム構成:
1. Investment Committee
   - Managing Partner
   - Investment Partners
   - Principal/Associate

2. Advisory Board
   - 業界著名人
   - 元大手VC/PE幹部
   - 成功起業家
   - 学術専門家

各メンバー情報:
- 顔写真・プロフィール
- 経歴・実績（詳細）
- 専門分野・担当セクター
- 過去の投資実績
- 学歴・資格
- 外部活動（講演・執筆）
- SNSリンク

投資哲学・コメント:
- 個人の投資観
- 業界への見解
- 注目している分野
- 投資先へのメッセージ
```

#### For Investors (/ventures/investors)
**LP向け限定情報エリア**

```
認証必須エリア:
- ログイン・会員登録機能
- LP認証・KYC対応
- 2FA・セキュリティ強化

提供情報:
1. Fund Performance
   - ファンド全体のパフォーマンス
   - IRR・MOIC・DPI等指標
   - ベンチマーク比較
   - リスク調整済みリターン

2. Portfolio Details
   - 投資先詳細レポート
   - 財務・事業KPI
   - 評価額推移
   - Exit予定・戦略

3. Market Analysis
   - セクター分析レポート
   - 市場動向・予測
   - 競合分析
   - リスク要因分析

4. Regular Reports
   - 四半期レポート
   - 年次報告書
   - マンスリーアップデート
   - 臨時レポート

5. Events & Communications
   - LP限定イベント
   - 投資先紹介セッション
   - 市場勉強会
   - 1on1ミーティング申込

6. Documents
   - ファンド基本合意書
   - 法的文書
   - 税務関連情報
   - コンプライアンス文書
```

### 2. Services詳細ページ（各サービス独立）

### 3. Media (/media) - 「主力事業：Crypto Times」

#### About Crypto Times (/media/about)
**2018年創刊、日本最大級のWeb3専門メディア**

```
メディア概要:
- 創刊: 2018年
- 業界ポジション: 日本最大級のWeb3専門メディア
- 月間PV: XXX万（具体的数値）
- 登録会員数: XX万人
- 記事数: 10,000本以上

歴史・マイルストーン:
- 2018年: Crypto Times創刊
- 2019年: 月間100万PV達成
- 2020年: DeFi特集で業界をリード
- 2021年: NFT/GameFi分野の報道強化
- 2022年: 大手取引所との提携
- 2023年: AIxWeb3の最先端報道
- 2024年: RWA・規制動向の専門報道

メディア実績:
- 独占インタビュー: Vitalik Buterin、CZ、Sam Altman等
- 特集シリーズ: DeFi革命、NFT市場分析、規制動向等
- 速報実績: 重要プロトコルローンチ、規制発表等
- 業界初報道: 複数の重要ニュースで業界初報道

読者層・影響力:
- 読者属性:
  - 投資家・トレーダー: 35%
  - 開発者・エンジニア: 25%
  - 事業者・経営者: 20%
  - 研究者・学生: 10%
  - その他: 10%
- 地域分布:
  - 日本: 60%
  - アジア: 25%
  - 欧米: 15%

編集方針・価値:
- 正確性: ファクトチェック体制
- 速報性: 24時間体制での情報収集
- 専門性: 技術的深度のある解説
- 中立性: 特定プロジェクトに偏らない報道
- 教育性: 初心者にも分かりやすい解説
```

#### Editorial Policy (/media/editorial-policy)
**編集方針・ジャーナリズム基準**

```
編集理念:
- Web3業界の健全な発展に貢献
- 正確で公正な情報提供
- 読者の投資判断・事業判断を支援
- 技術革新と規制のバランスを重視

報道基準:
1. 正確性の確保
   - 複数ソースによる裏付け
   - 専門家によるレビュー
   - 誤報時の迅速な訂正

2. 中立性・公正性
   - 広告主からの編集独立
   - 利益相反の開示
   - 批判的視点の維持

3. 専門性の追求
   - 技術的正確性の重視
   - 業界用語の適切な解説
   - 深度のある分析記事

4. 倫理規定
   - インサイダー情報の取り扱い
   - プライバシー保護
   - 著作権遵守

コンテンツカテゴリ:
- ニュース（速報・日次）
- 分析・解説記事
- インタビュー・対談
- 技術解説・チュートリアル
- 市場レポート
- 規制・政策分析
- イベントレポート
```

#### Advertising & Partnership (/media/advertising)
**広告・パートナーシップ機会**

```
広告メニュー:
1. ディスプレイ広告
   - トップページバナー
   - 記事内広告
   - サイドバー広告
   - 料金: ¥XXX〜/月

2. スポンサードコンテンツ
   - PR記事作成・掲載
   - インタビュー記事
   - 事例紹介記事
   - 料金: ¥XXX〜/記事

3. メールマガジン広告
   - ヘッダー広告
   - 記事内広告
   - 専用配信
   - 料金: ¥XXX〜/配信

4. イベント協賛
   - カンファレンス共催
   - ウェビナー開催
   - ミートアップ支援
   - 料金: 要相談

パートナーシップ:
- コンテンツ提携
- データ連携
- 共同調査・レポート
- 海外メディア連携

広告主実績:
- 国内外大手取引所
- ブロックチェーンプロジェクト
- Web3関連企業
- 金融機関・VC

効果測定:
- インプレッション数
- クリック率・CTR
- コンバージョン追跡
- ブランドリフト調査
```

#### Media Kit (/media/media-kit)
**メディア資料・統計情報**

```
メディア統計:
- 月間PV: XX万
- 月間UU: XX万
- 平均セッション時間: X分
- ページ/セッション: X.X
- リピート率: XX%

ソーシャルメディア:
- Twitter: XXK フォロワー
- Telegram: XXK メンバー
- Discord: XXK メンバー
- YouTube: XXK 登録者

コンテンツ実績:
- 月間記事本数: XXX本
- 独占記事率: XX%
- 翻訳記事: XX%（英語・中国語）
- 動画コンテンツ: XX本/月

メディア掲載・引用:
- 大手メディアからの引用: XXX回
- テレビ出演: XX回
- 政府・規制当局への情報提供: XX回
- 業界レポートでの言及: XX回

ダウンロード資料:
- メディアガイド（PDF）
- 料金表（PDF）
- 読者属性レポート（PDF）
- 成功事例集（PDF）
```

#### Consulting Services (/services/consulting)
**コンサルティング事業の詳細**

```
サービス領域:
1. Business Strategy
   - Web3事業戦略策定
   - 市場参入戦略
   - 競合分析・ポジショニング
   - 事業計画・ロードマップ

2. Token Economics
   - トークンエコノミクス設計
   - インセンティブモデル構築
   - 経済性シミュレーション
   - ガバナンス設計

3. Market Entry Support
   - 日本市場進出支援
   - 規制対応・コンプライアンス
   - パートナーシップ仲介
   - ローカライゼーション

4. Fundraising Support
   - 資金調達戦略
   - ピッチデッキ作成
   - 投資家紹介
   - デューデリジェンス対応

コンサルティング手法:
- データドリブンアプローチ
- 独自分析フレームワーク
- 業界ネットワーク活用
- ハンズオン支援

プロジェクト事例:
- 代表的成功事例（匿名化）
- 課題→解決→成果の流れ
- 期間・チーム構成
- クライアントの声

料金体系:
- 戦略コンサルティング: ¥XX/月〜
- プロジェクトベース: ¥XXM〜
- 成功報酬型: 要相談
- リテイナー契約: ¥XX/月

コンサルタント紹介:
- 各領域の専門家
- 経歴・実績・専門分野
- 担当可能プロジェクト
- クライアントからの評価
```

#### Development Services (/services/development)
**開発事業の詳細**

```
開発領域:
1. Blockchain Development
   - スマートコントラクト開発
   - DeFiプロトコル構築
   - NFTプラットフォーム
   - DAO構築支援

2. dApp Development
   - フロントエンド開発
   - ウォレット連携
   - UI/UX設計
   - モバイルアプリ対応

3. Infrastructure Development
   - ブロックチェーンインフラ
   - ノード運用・管理
   - API開発・提供
   - セキュリティ監査

4. Web Development
   - 企業サイト構築
   - ECサイト・マーケットプレイス
   - 管理画面・ダッシュボード
   - CMS・コンテンツ管理

技術スタック:
- ブロックチェーン: Ethereum, Solana, Polygon, BSC
- 言語: Solidity, Rust, TypeScript, Python
- フレームワーク: React, Next.js, Vue.js
- データベース: PostgreSQL, MongoDB, Redis
- インフラ: AWS, GCP, Vercel, Docker

開発プロセス:
- 要件定義・設計
- プロトタイプ開発
- 開発・テスト
- セキュリティ監査
- デプロイ・運用サポート

開発実績:
- 代表的開発プロジェクト
- 技術的挑戦・革新
- パフォーマンス・品質指標
- クライアント満足度

セキュリティ対策:
- コードレビュー体制
- セキュリティ監査プロセス
- 脆弱性対応・パッチ適用
- ペネトレーションテスト

料金・期間:
- MVP開発: ¥XXM〜（X週間）
- フル開発: ¥XXM〜（XX週間）
- 保守・運用: ¥XX/月〜
- セキュリティ監査: ¥XX〜
```

#### Research & Analytics (/services/research)
**リサーチ・分析事業の詳細**

```
リサーチ領域:
1. Market Research
   - 市場規模・成長予測
   - 競合分析・ベンチマーク
   - ユーザー動向・行動分析
   - 規制環境・政策影響

2. Technical Analysis
   - プロトコル分析・評価
   - セキュリティ分析
   - パフォーマンス評価
   - 技術トレンド調査

3. Investment Research
   - 投資機会分析
   - 企業評価・デューデリジェンス
   - セクター動向・予測
   - リスク分析・評価

4. Custom Research
   - クライアント特化調査
   - 特定テーマ深掘り
   - 定量・定性分析
   - レポート・提言作成

調査手法:
- 一次データ収集
- 業界専門家インタビュー
- サーベイ・アンケート調査
- オンチェーンデータ分析
- 競合・事例分析

レポート種類:
- 市場レポート（四半期・年次）
- セクターレポート
- 企業分析レポート
- 技術調査レポート
- カスタムレポート

データソース:
- 独自調査データ
- パートナー機関データ
- オンチェーンデータ
- 公開統計・資料
- 業界専門家ネットワーク

クライアント事例:
- 投資判断支援
- 新規事業検討
- 市場参入戦略
- リスク評価
- 政策提言
```

### 3. Works (/works) - 「実績・成功事例」

#### 投資実績（Ventures）
```
Exit成功事例:
- IPO実績（会社名・時期・リターン）
- M&A実績（買収額・リターン倍率）
- セカンダリー売却実績

成長企業事例:
- 評価額成長（投資時→現在）
- 事業成長指標（売上・ユーザー数等）
- 市場インパクト・業界地位

投資プロセス事例:
- 発掘→評価→投資→支援の流れ
- デューデリジェンス内容
- 投資委員会での判断基準
- 投資後のハンズオン支援
```

#### 事業支援実績（Services）
```
コンサルティング事例:
- 戦略策定支援
- 資金調達支援
- 市場参入支援
- 組織・人材支援

開発実績:
- dApp・プロトコル開発
- インフラ構築
- セキュリティ監査
- システム統合

メディア実績:
- 独占取材・インタビュー
- 市場予測・分析記事
- 業界への影響・引用
- イベント・カンファレンス
```

## 🎨 デザイン・UX戦略（投資事業特化）

### デザインコンセプト
**「信頼性 × 先進性 × 透明性」**
- 投資家向けの信頼感・安心感
- Web3業界らしい先進性・革新性
- 情報開示の透明性・誠実性

### カラーパレット（投資事業向け）
```css
/* Primary Colors - 信頼・安定 */
Primary: #1E3A8A (深いネイビー - 金融業界の信頼性)
Secondary: #3B82F6 (ロイヤルブルー - テクノロジー)
Accent: #10B981 (エメラルドグリーン - 成長・成功)

/* Supporting Colors */
Dark: #0F172A (ダークグレー)
Light: #F8FAFC (ライトグレー)
Warning: #F59E0B (アンバー - 注意・リスク)
Success: #059669 (グリーン - 成功・利益)
Error: #DC2626 (レッド - 損失・リスク)

/* Data Visualization */
Chart1: #6366F1 (インディゴ)
Chart2: #8B5CF6 (バイオレット)
Chart3: #EC4899 (ピンク)
Chart4: #14B8A6 (ティール)
```

### タイポグラフィ（投資業界標準）
```css
/* Primary Font */
Headings: "Inter" (モダン・可読性重視)
Body: "Inter" / "Noto Sans JP"
Data/Numbers: "JetBrains Mono" (数値データ用)

/* Font Sizes */
H1: 3.5rem / 56px (Hero・ランディング)
H2: 2.25rem / 36px (セクション見出し)
H3: 1.5rem / 24px (サブセクション)
Body: 1rem / 16px (本文)
Caption: 0.875rem / 14px (キャプション)
```

### 投資データ可視化デザイン
```
チャート・グラフ:
- パフォーマンスダッシュボード
- ポートフォリオ分散円グラフ
- 投資リターン推移グラフ
- セクター別投資比率
- 時系列パフォーマンス比較

インフォグラフィック:
- 投資プロセス図解
- 投資哲学・戦略説明
- 市場分析・予測図表
- リスク・リターン分析
```

## 🔧 B2B・投資家向け特化機能

### 1. 投資家認証・管理システム

**LP限定エリア認証**:
```typescript
// 認証レベル定義
interface UserRole {
  public: 一般ユーザー
  investor: 認定投資家
  lp: リミテッドパートナー
  admin: 管理者
}

// アクセス制御
const accessControl = {
  '/ventures/investors': ['lp', 'admin'],
  '/ventures/reports': ['investor', 'lp', 'admin'],
  '/ventures/portfolio/details': ['lp', 'admin']
}
```

**KYC・AML対応**:
```
必須提出書類:
- 身分証明書（運転免許証・パスポート）
- 住所証明書（住民票・公共料金請求書）
- 財産証明書（残高証明・年収証明）
- 反社会的勢力非該当証明
- 投資経験・リスク許容度調査

認証プロセス:
1. オンライン申請フォーム
2. 書類アップロード・確認
3. ビデオ本人確認
4. 審査・承認（3-5営業日）
5. アカウント有効化・ログイン
```

### 2. 投資情報管理システム

**ポートフォリオ管理**:
```typescript
interface PortfolioCompany {
  id: string
  name: string
  sector: string[]
  investmentStage: 'seed' | 'series-a' | 'series-b' | 'series-c'
  investmentDate: Date
  investmentAmount: number // LP向けのみ
  currentValuation: number // LP向けのみ
  ownership: number // LP向けのみ
  status: 'active' | 'exited' | 'struggling'
  
  // 公開情報
  publicInfo: {
    description: string
    website: string
    logo: string
    tags: string[]
  }
  
  // 限定情報（LP向け）
  privateInfo?: {
    financials: QuarterlyFinancials[]
    kpis: PerformanceMetrics[]
    risks: RiskAssessment[]
    exitStrategy: ExitPlan
  }
}
```

**パフォーマンス追跡**:
```typescript
interface FundPerformance {
  fundName: string
  vintage: number
  totalCommitment: number
  totalInvested: number
  totalReturned: number
  
  // パフォーマンス指標
  irr: number // 内部収益率
  moic: number // 投資倍率
  dpi: number // 分配倍率
  rvpi: number // 残存価値倍率
  
  // ベンチマーク比較
  benchmarkComparison: {
    industry: string
    outperformance: number
  }
}
```

### 3. リード獲得・営業支援システム

**投資家向けリード獲得**:
```
ファネル設計:
1. 認知: メディア記事・SNS・イベント
2. 興味: 投資レポート・市場分析ダウンロード
3. 検討: ウェビナー参加・1on1面談
4. 意思決定: ファンド説明資料・利回り試算
5. 投資実行: LP契約・資金払込

リードスコアリング:
- 資産規模・投資経験
- Web3/ブロックチェーン理解度
- 投資目的・期間
- リスク許容度
- 過去の投資実績
```

**投資先候補企業向け**:
```
申請フォーム項目:
- 会社概要・事業内容
- チーム・経営陣情報
- プロダクト・技術詳細
- 市場・競合分析
- 財務状況・資金使途
- 調達希望額・条件
- ピッチデッキ・事業計画書

スクリーニングプロセス:
1. 書類選考（3-5営業日）
2. 初回面談（30分）
3. 詳細面談・DD（2週間）
4. 投資委員会（週次）
5. 投資実行・契約（1-2週間）
```

### 4. 投資家向けコミュニケーション

**定期レポート自動配信**:
```typescript
interface ReportSchedule {
  monthly: {
    recipients: ['all-lps']
    content: 'ポートフォリオアップデート'
    deliveryDate: '月末から5営業日以内'
  }
  
  quarterly: {
    recipients: ['all-lps', 'investors']
    content: 'パフォーマンスレポート'
    deliveryDate: '四半期末から10営業日以内'
  }
  
  annual: {
    recipients: ['all-lps']
    content: '年次報告書・監査済み財務諸表'
    deliveryDate: '年度末から30日以内'
  }
  
  adhoc: {
    triggers: ['重要な投資実行', 'Exit実現', '市場急変']
    recipients: '投資家レベル別'
    deliveryTime: '24時間以内'
  }
}
```

**イベント・ミーティング管理**:
```
LP向けイベント:
- 四半期LP会議（オンライン・オフライン）
- 年次総会・懇親会
- 投資先企業紹介セッション
- 業界動向勉強会・セミナー

個別面談システム:
- Calendly統合予約システム
- LP個別相談枠（月次）
- 投資先企業CEO面談機会
- 業界専門家との勉強会
```

## 📊 投資事業特化KPI・成果測定

### 投資事業KPI

**ファンドパフォーマンス**:
```
目標値:
- ファンドIRR: 25%+（年率）
- ファンドMOIC: 3.0x+（5年間）
- 成功投資比率: 70%+
- Exit実現率: 30%+（3年以内）

ベンチマーク:
- 日本VC業界平均
- グローバルWeb3ファンド
- 同ステージファンド比較
```

**投資活動KPI**:
```
目標値:
- 年間投資実行件数: 10-15件
- 平均投資額: ¥50M-200M
- デューデリジェンス期間: 平均4週間
- 投資委員会承認率: 25%
```

**LP・投資家関係**:
```
目標値:
- LP満足度: 90%+
- 出資継続率: 85%+
- 新規LP獲得: 年間5-10件
- 解約率: <5%/年
```

### Webサイト・マーケティングKPI

**投資家向けリード**:
```
目標値:
- 投資家問い合わせ: 月間20件
- LP面談実施率: 50%
- LP契約成約率: 25%
- 平均出資額: ¥100M
```

**投資先候補リード**:
```
目標値:
- 投資申込件数: 月間30件
- 書類選考通過率: 20%
- 面談実施率: 80%
- 投資実行率: 15%
```

**メディア・ブランディング**:
```
目標値:
- Crypto Times月間PV: 500K
- SNSフォロワー総数: 50K
- メディア掲載: 月間5件
- イベント登壇: 四半期3件
```

## 🚀 開発ロードマップ（16週間）

### Phase 1: 基盤構築・設計（4週間）
```
Week 1: 要件最終確認・設計
- 投資事業要件詳細化
- ナビゲーション構造確定
- デザインシステム設計
- セキュリティ設計

Week 2: 環境・認証システム
- Next.js + Sanity環境構築
- 多言語対応実装（next-intl）
- NextAuth.js認証実装
- LP専用エリア基盤

Week 3: 基本レイアウト・コンポーネント
- レスポンシブナビゲーション
- ハンバーガーメニュー実装
- 基本デザインシステム
- 共通コンポーネント

Week 4: ホームページ・基本ページ
- ホームページ（投資事業強調）
- About基本構造
- Contact基本機能
- 投資家向けCTA
```

### Phase 2: 投資事業ページ開発（6週間）
```
Week 5: Ventures メインページ
- Investment Philosophy
- Portfolio概要ページ
- Investment Team紹介
- For Investors入口

Week 6: Portfolio詳細システム
- 投資先企業管理システム
- フィルタリング・検索機能
- 公開/限定情報の使い分け
- パフォーマンスデータ表示

Week 7: LP向け限定エリア
- 認証・権限管理システム
- ファンドパフォーマンス表示
- レポート配信システム
- ドキュメント管理

Week 8: 投資データ可視化
- パフォーマンスダッシュボード
- チャート・グラフ実装
- データ分析・レポート機能
- Excel/PDF出力機能

Week 9: Services詳細ページ（前半）
- Crypto Times詳細
- Consulting Services詳細
- 実績・事例表示システム
- サービス比較機能

Week 10: Services詳細ページ（後半）
- Development Services詳細
- Research & Analytics詳細
- 料金・見積もりシステム
- お問い合わせフォーム統合
```

### Phase 3: コンテンツ・機能拡充（4週間）
```
Week 11: Works・実績ページ
- 投資実績表示システム
- 事業支援実績
- 成功事例詳細
- フィルタリング・検索

Week 12: Insights・ブログシステム
- 投資インサイト記事
- 市場分析レポート
- カテゴリ・タグ機能
- 検索・推薦機能

Week 13: Newsroom・多言語
- プレスリリース管理
- メディア掲載実績
- 多言語コンテンツ実装
- hreflang・SEO最適化

Week 14: 高度機能・統合
- 投資家向けメール配信
- Calendly統合（面談予約）
- CRM連携（Notion API）
- アナリティクス実装
```

### Phase 4: テスト・ローンチ・運用（2週間）
```
Week 15: 総合テスト・セキュリティ
- 全機能統合テスト
- LP向け機能テスト
- セキュリティ監査
- パフォーマンステスト
- アクセシビリティ確認

Week 16: ローンチ・運用開始
- 本番環境デプロイ
- DNS・SSL設定
- 監視・ログ設定
- コンテンツ最終確認
- ソフトローンチ・フィードバック
```

## 💡 将来拡張計画（投資事業特化）

### 短期（3ヶ月以内）
```
投資家向け機能:
- モバイルアプリ（iOS/Android）
- リアルタイム通知システム
- AIチャットボット（投資相談）
- ビデオ会議システム統合

LP向け高度機能:
- カスタムレポート生成
- API連携（会計システム）
- 税務計算・支援機能
- ベンチマーク分析ツール
```

### 中期（6ヶ月以内）
```
投資管理システム:
- CRM統合（Salesforce/HubSpot）
- 投資先管理システム
- デューデリジェンス支援ツール
- 契約・法務文書管理

データ分析・AI:
- 投資先スクリーニングAI
- 市場予測・分析AI
- リスク評価自動化
- ポートフォリオ最適化提案
```

### 長期（1年以内）
```
エコシステム構築:
- 投資先企業向けポータル
- LP向けネットワーキング機能
- 業界データプラットフォーム
- 投資教育・啓蒙コンテンツ

グローバル展開:
- 海外LP向け機能
- 多通貨対応
- 各国規制対応
- 現地パートナー連携
```

## 🚨 投資事業特化リスク管理

### 規制・法的リスク
```
対策:
- 金融商品取引法対応
- 投資事業有限責任組合法対応
- 暗号資産関連規制対応
- プライバシー・データ保護法対応
- 反社会的勢力排除体制

継続監視:
- 法規制動向モニタリング
- 業界ガイドライン更新対応
- 自主規制団体対応
- 当局コミュニケーション
```

### セキュリティ・プライバシーリスク
```
対策:
- LP情報暗号化・保護
- 投資情報アクセス制御
- ログ監視・異常検知
- バックアップ・DR計画
- セキュリティ監査（年2回）

インシデント対応:
- 24時間監視体制
- 緊急対応チーム
- LP向け緊急連絡体制
- 被害状況報告・対策
```

### 風評・レピュテーションリスク
```
対策:
- 透明性の高い情報開示
- 定期的なLP向け報告
- メディア対応体制
- クライシスコミュニケーション計画
- SNS・オンライン監視

対応計画:
- 風評モニタリング
- 迅速な事実確認・公表
- ステークホルダー向け説明
- 法的対応検討
- 再発防止策実施
```

---

## 📝 更新履歴

- **v3.1** (2025-07-07): 主力事業をCrypto Times（メディア事業）に修正
- **v3.0** (2025-07-07): 投資事業強化・サービス詳細展開・ナビゲーション刷新
- **v2.0** (2025-07-07): 事業内容更新・ドメイン変更・完全改訂版
- **v1.0** (2025-07-07): 初版作成

---

**作成日**: 2025-07-07  
**バージョン**: v3.1  
**ドメイン**: rokubunnoni.com  
**作成者**: Claude Code with Gemini consultation  
**対象**: 株式会社ロクブンノニ 法人Webサイト（メディア事業中心版）