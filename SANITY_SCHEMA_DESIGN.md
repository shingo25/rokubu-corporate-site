# Sanity CMS スキーマ設計書
## 株式会社ロクブンノニ 法人サイト

## 🏗️ 概要

### CMSの役割
- **多言語コンテンツ管理** (日本語・英語・中国語)
- **B2Bコンテンツ配信** (サービス・事例・インサイト)
- **リード獲得支援** (資料・フォーム管理)
- **権威性構築** (実績・メディア掲載・チーム情報)

### 多言語対応戦略
- `@sanity/document-internationalization`プラグイン使用
- 言語別ドキュメント管理
- 翻訳ワークフロー対応
- SEO最適化対応

## 📋 ドキュメントタイプ定義

### 1. 基本情報系

#### company (会社情報)
```typescript
{
  _type: 'company',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    companyName: string,
    companyNameEn: string,
    tagline: string,
    description: text,
    establishedYear: number,
    capital: string,
    employeeCount: string,
    
    // 連絡先
    address: {
      postalCode: string,
      prefecture: string,
      city: string,
      street: string,
      building: string
    },
    phone: string,
    email: string,
    
    // ビジュアル
    logo: image,
    favicon: image,
    
    // SNS
    socialLinks: [{
      platform: string,
      url: url
    }],
    
    // SEO
    seoTitle: string,
    seoDescription: string,
    ogImage: image
  }
}
```

#### teamMember (チームメンバー)
```typescript
{
  _type: 'teamMember',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    fullName: string,
    fullNameEn: string,
    position: string,
    department: string,
    joinDate: date,
    
    // プロフィール
    bio: text,
    expertise: [string],
    education: [{
      institution: string,
      degree: string,
      year: number
    }],
    experience: [{
      company: string,
      position: string,
      period: string,
      description: text
    }],
    
    // ビジュアル
    photo: image,
    
    // SNS・外部リンク
    linkedIn: url,
    twitter: url,
    website: url,
    
    // 表示設定
    isExecutive: boolean,
    displayOrder: number,
    isPublic: boolean
  }
}
```

### 2. サービス・事業系

#### service (サービス)
```typescript
{
  _type: 'service',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    title: string,
    slug: slug,
    subtitle: string,
    description: text,
    
    // 詳細
    overview: richText,
    features: [{
      title: string,
      description: text,
      icon: image
    }],
    benefits: [string],
    process: [{
      step: number,
      title: string,
      description: text
    }],
    
    // 価格・期間
    pricing: {
      type: string, // 'consultation' | 'project' | 'retainer'
      startingPrice: string,
      currency: string,
      note: string
    },
    duration: string,
    
    // ビジュアル
    heroImage: image,
    gallery: [image],
    
    // 関連情報
    targetAudience: [string],
    industryFocus: [string],
    technologies: [string],
    
    // CTA
    ctaText: string,
    ctaType: string, // 'contact' | 'calendar' | 'download'
    
    // SEO
    seoTitle: string,
    seoDescription: string,
    ogImage: image,
    
    // 表示設定
    isFeatured: boolean,
    displayOrder: number,
    isActive: boolean
  }
}
```

#### caseStudy (導入事例)
```typescript
{
  _type: 'caseStudy',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    title: string,
    slug: slug,
    subtitle: string,
    summary: text,
    
    // クライアント情報
    client: {
      name: string,
      industry: string,
      size: string, // 'startup' | 'scale-up' | 'enterprise'
      country: string,
      logo: image,
      isAnonymous: boolean
    },
    
    // プロジェクト詳細
    challenge: richText,
    solution: richText,
    results: richText,
    
    // 数値的成果
    metrics: [{
      label: string,
      value: string,
      unit: string,
      description: string
    }],
    
    // プロジェクト情報
    services: [reference('service')],
    duration: string,
    teamSize: number,
    technologies: [string],
    
    // タイムライン
    timeline: [{
      phase: string,
      duration: string,
      description: text,
      deliverables: [string]
    }],
    
    // ビジュアル
    heroImage: image,
    beforeAfterImages: [{
      before: image,
      after: image,
      caption: string
    }],
    gallery: [image],
    
    // 証言
    testimonial: {
      quote: text,
      author: string,
      position: string,
      photo: image
    },
    
    // SEO
    seoTitle: string,
    seoDescription: string,
    ogImage: image,
    
    // 表示設定
    isFeatured: boolean,
    displayOrder: number,
    isPublic: boolean,
    
    // フィルタリング用
    categories: [string],
    tags: [string]
  }
}
```

### 3. コンテンツ系

#### insight (インサイト記事)
```typescript
{
  _type: 'insight',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    title: string,
    slug: slug,
    excerpt: text,
    content: richText,
    
    // 記事情報
    category: string, // 'market-report' | 'case-analysis' | 'regulatory-update'
    tags: [string],
    readingTime: number,
    
    // 著者情報
    author: reference('teamMember'),
    coAuthors: [reference('teamMember')],
    publishedAt: datetime,
    updatedAt: datetime,
    
    // ビジュアル
    featuredImage: image,
    gallery: [image],
    
    // ダウンロード資料
    downloadableAssets: [{
      title: string,
      file: file,
      description: text,
      requiresEmail: boolean
    }],
    
    // 関連情報
    relatedServices: [reference('service')],
    relatedCaseStudies: [reference('caseStudy')],
    relatedInsights: [reference('insight')],
    
    // SEO
    seoTitle: string,
    seoDescription: string,
    ogImage: image,
    
    // 表示設定
    isFeatured: boolean,
    isDraft: boolean,
    isPublic: boolean
  }
}
```

#### page (一般ページ)
```typescript
{
  _type: 'page',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    title: string,
    slug: slug,
    description: text,
    
    // コンテンツ
    content: richText,
    sections: [{
      _type: 'section',
      sectionType: string,
      title: string,
      content: richText,
      image: image,
      ctaButton: {
        text: string,
        link: string,
        type: string
      }
    }],
    
    // ビジュアル
    heroImage: image,
    
    // SEO
    seoTitle: string,
    seoDescription: string,
    ogImage: image,
    
    // 表示設定
    isPublic: boolean,
    showInNavigation: boolean,
    navigationOrder: number
  }
}
```

### 4. 実績・権威性系

#### pressMedia (メディア掲載)
```typescript
{
  _type: 'pressMedia',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    title: string,
    mediaName: string,
    publishedDate: date,
    url: url,
    
    // 詳細
    description: text,
    category: string, // 'interview' | 'feature' | 'news' | 'opinion'
    language: string,
    
    // ビジュアル
    mediaLogo: image,
    screenshot: image,
    
    // 表示設定
    isFeatured: boolean,
    displayOrder: number
  }
}
```

#### award (受賞・認定)
```typescript
{
  _type: 'award',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    title: string,
    organization: string,
    awardDate: date,
    category: string,
    
    // 詳細
    description: text,
    criteria: text,
    
    // ビジュアル
    badge: image,
    certificate: file,
    
    // 表示設定
    isFeatured: boolean,
    displayOrder: number
  }
}
```

#### partner (パートナー企業)
```typescript
{
  _type: 'partner',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    companyName: string,
    partnershipType: string, // 'strategic' | 'technology' | 'channel'
    startDate: date,
    
    // 詳細
    description: text,
    collaborationAreas: [string],
    
    // ビジュアル
    logo: image,
    
    // リンク
    website: url,
    
    // 表示設定
    isFeatured: boolean,
    displayOrder: number,
    isActive: boolean
  }
}
```

### 5. リード獲得系

#### downloadableResource (ダウンロード資料)
```typescript
{
  _type: 'downloadableResource',
  name: string,
  languages: ['ja', 'en', 'zh-CN'],
  fields: {
    // 基本情報
    title: string,
    description: text,
    resourceType: string, // 'whitepaper' | 'case-study' | 'brochure' | 'report'
    
    // ファイル
    file: file,
    previewImage: image,
    pageCount: number,
    fileSize: string,
    
    // リード獲得設定
    requiresRegistration: boolean,
    requiredFields: [{
      fieldName: string,
      isRequired: boolean
    }],
    
    // 分析
    downloadCount: number,
    
    // 表示設定
    isFeatured: boolean,
    isActive: boolean,
    displayOrder: number
  }
}
```

#### contactInquiry (問い合わせ)
```typescript
{
  _type: 'contactInquiry',
  fields: {
    // 基本情報
    inquiryType: string, // 'partnership' | 'service' | 'media' | 'other'
    subject: string,
    message: text,
    
    // 連絡先情報
    companyName: string,
    contactPerson: string,
    position: string,
    email: string,
    phone: string,
    country: string,
    
    // プロジェクト情報
    projectBudget: string,
    projectTimeline: string,
    servicesOfInterest: [string],
    
    // 管理情報
    submittedAt: datetime,
    status: string, // 'new' | 'in-progress' | 'replied' | 'closed'
    assignedTo: reference('teamMember'),
    notes: text,
    
    // GDPR対応
    consentToStore: boolean,
    consentToMarketing: boolean
  }
}
```

## 🔧 カスタムフィールド定義

### richText (リッチテキスト)
```typescript
richText: {
  type: 'array',
  of: [
    {
      type: 'block',
      styles: [
        {title: 'Normal', value: 'normal'},
        {title: 'H2', value: 'h2'},
        {title: 'H3', value: 'h3'},
        {title: 'Quote', value: 'blockquote'}
      ],
      marks: {
        decorators: [
          {title: 'Strong', value: 'strong'},
          {title: 'Emphasis', value: 'em'},
          {title: 'Code', value: 'code'}
        ],
        annotations: [
          {
            title: 'URL',
            name: 'link',
            type: 'object',
            fields: [
              {name: 'href', type: 'url', title: 'URL'},
              {name: 'blank', type: 'boolean', title: 'Open in new tab?'}
            ]
          }
        ]
      }
    },
    {
      type: 'image',
      fields: [
        {name: 'alt', type: 'string', title: 'Alt text'},
        {name: 'caption', type: 'string', title: 'Caption'}
      ]
    }
  ]
}
```

### localizedString (多言語文字列)
```typescript
localizedString: {
  type: 'object',
  fields: [
    {name: 'ja', type: 'string', title: '日本語'},
    {name: 'en', type: 'string', title: 'English'},
    {name: 'zh', type: 'string', title: '中文'}
  ]
}
```

## 🌐 多言語設定

### 国際化プラグイン設定
```javascript
// sanity.config.js
import {documentInternationalization} from '@sanity/document-internationalization'

export default defineConfig({
  plugins: [
    documentInternationalization({
      supportedLanguages: [
        {id: 'ja', title: '日本語'},
        {id: 'en', title: 'English'},
        {id: 'zh-CN', title: '中文（简体）'}
      ],
      schemaTypes: ['service', 'caseStudy', 'insight', 'page', 'company', 'teamMember']
    })
  ]
})
```

### 翻訳ワークフロー
1. **原文作成**: 日本語でオリジナルコンテンツ作成
2. **翻訳依頼**: Sanity上で他言語版ドキュメント作成
3. **翻訳実施**: 専門翻訳者による翻訳
4. **レビュー**: ネイティブスピーカーによる最終確認
5. **公開**: 多言語版同時公開

## 🔍 検索・フィルタリング設定

### 検索インデックス
```javascript
// 検索対象フィールド定義
searchableFields: [
  'title',
  'description', 
  'content',
  'tags',
  'categories'
]
```

### フィルタリング項目
- **サービス**: カテゴリ、対象業界、技術
- **事例**: 業界、企業規模、サービス種別
- **インサイト**: カテゴリ、タグ、著者
- **言語**: 全コンテンツタイプ

## 📊 アナリティクス・トラッキング

### コンテンツパフォーマンス
- ページビュー数
- 滞在時間
- ダウンロード数
- 問い合わせ発生率

### SEO分析
- 検索流入キーワード
- メタデータ最適化状況
- 構造化データ対応状況

---

**作成日**: 2025-07-07  
**バージョン**: v1.0  
**対象**: 株式会社ロクブンノニ 法人Webサイト  
**CMS**: Sanity Studio