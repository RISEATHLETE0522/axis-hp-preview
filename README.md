# FOOTBALL SCHOOL AXiS 公式サイト

茨木市・高槻市で活動するサッカースクール「FOOTBALL SCHOOL AXiS」の公式ホームページ(静的HTML)。
2026-07-11 制作。情報ソースは公式Instagram(@football_school_axis)と旧公式ページ(sgrum)。
テスト公開中: https://riseathlete0522.github.io/axis-hp-preview/ (noindex付き)

## 構成

| ファイル | 役割 |
|---------|------|
| index.html | トップ(ヒーロー/コンセプト/強み/コーチ/スクール概要/パーソナル/Instagram/キャンペーン/体験フロー/CTA) |
| about.html | コンセプト・メソッド・コーチ詳細・ウェアの由来 |
| school.html | クラス・料金・アクセス・入会の流れ・FAQ(FAQPage構造化データ入り) |
| personal.html | パーソナルトレーニング・コーチ派遣 |
| contact.html | 無料体験・お問い合わせ(LINE/電話/Instagram DM) |
| assets/ | css / js / img(Instagram取得写真をWeb用に最適化済) |

## 公開前に必ずやること

1. **ドメイン置換**: 全HTML・sitemap.xml・robots.txt 内の `https://www.fs-axis.jp` を実ドメインに一括置換
   (各HTMLの `<!-- TODO -->` コメント参照。canonical / og:url / og:image / JSON-LD が対象)
2. **月会費の確定**: school.html の料金セクションは「公式LINEにてご案内」としている。
   正式な月会費が決まれば数字に差し替え
3. **写真の権利確認**: 写真はスクール公式Instagramから取得。スクール(=本人たち)の公式サイトでの
   利用を前提としているが、掲載児童の保護者許諾はスクール側で確認済みであること
4. 公開後、Google Search Console にサイトマップ登録+Instagramプロフィールのリンクを新URLに変更

## 検証済み(2026-07-11 ローカル)

- Lighthouse(モバイル): index 91 / school 95(Performance)、Accessibility・Best Practices・SEO 全ページ100
- Lighthouse(デスクトップ): index Performance 99
- リンク切れ 0 / OGP・meta 全ページ充足 / JSON-LD パースOK / 375・768・1280px 横スクロールなし

## ローカル確認方法

```bash
cd axis-soccer-hp
python3 -m http.server 8930
# → http://localhost:8930/
```
