# japan-care-facilities：日本の介護施設数・介護保険料データ（都道府県・市区町村別 CSV）

厚生労働省「介護サービス情報公表システム」のオープンデータなどをもとに [介護施設相場.com](https://kaigo-souba.com/) が集計した、**全国・47都道府県・約1,900市区町村**の介護施設数（種類別）・定員・運営法人・在宅サービス事業所数・介護保険料・要介護認定率・高齢者人口の CSV です。

- データの説明とダウンロード：https://kaigo-souba.com/data/
- サイトで見る（都道府県・市区町村のページ）：https://kaigo-souba.com/
- 更新：このリポジトリの CSV は、毎日サイトの `/data/` から自動で取り込んでいます。サイトは毎月12日に公表元を確認して自動更新します。施設データは年2回（6月末・12月末時点）、人口は年1回（1月1日現在）、介護保険料は3年ごと（第9期は2024〜2026年度）の公表です。

## ファイル

| ファイル | 内容 |
|-|-|
| `data/prefecture.csv` | 全国（00）・47都道府県 |
| `data/municipality.csv` | 市区町村（政令市とその区・東京23区を含む） |

文字コードは UTF-8（BOM 付き）で、Excel でそのまま開けます。市区町村コードは6桁の全国地方公共団体コード。区分は「市」「町」「村」「特別区」「政令市」「政令市の区」で、政令市は市の行と区の行の両方があります。

## 主な列

| 列名 | 意味 | Description |
|-|-|-|
| 施設数_合計・施設数_特養 など7種類 | 介護保険の指定を受けた入所・入居型の事業所数（特養・老健・介護医療院・介護付き有料・サ高住（介護付き）・ケアハウス・グループホーム）。住宅型有料老人ホームや一般型サ高住は含まない | number of residential care facilities |
| 定員_合計_参考・定員の入力がある施設数 | 定員は入力のある施設だけの合計（参考値） | reported capacity (reference only) |
| 事業所数_デイサービス・訪問介護・居宅介護支援 | 在宅サービスの事業所数 | home-care offices |
| 運営_社会福祉法人 など6区分 | 運営法人の種類別の施設数 | facilities by operator type |
| 人口・65歳以上人口・75歳以上人口・85歳以上人口・高齢化率_% | 住民基本台帳人口 | resident population |
| 65歳以上1万人あたり施設数 | 施設数÷65歳以上人口×10,000 | facilities per 10,000 people aged 65+ |
| 介護保険料_第9期_月額_円・第8期・変化率_% | 第1号保険料基準額（月額） | monthly LTC insurance premium (yen) |
| 要介護認定率_% | 要介護（要支援）認定率 | certification rate (%) |
| 介護保険料の注記 | 「市の額」＝政令市の区、「都道府県平均」＝市町村別の額が公表されていない地域 | note on premium |
| 参考値 | 1＝65歳以上人口が2,000人未満で変動が大きい | 1 = fewer than 2,000 people aged 65+ |

全列の英語の説明は https://kaigo-souba.com/data/ にあります。集計方法の詳細は https://kaigo-souba.com/about/ を見てください。

## 利用条件（ライセンス）

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.ja)。商用・非商用を問わず、報道・ブログ・研究・授業・アプリ・AI の学習や回答などに自由に使えます。条件は出典を明記することだけです。

**「出典を明記する」とは？** 使った数字がどこのデータかを、読む人に分かるように書き添えることです。次の1行をコピーして、数字や表・グラフのすぐ下か、記事・資料の最後に貼り付けてください。

```
出典：介護施設相場.com（厚生労働省「介護サービス情報公表システム」等をもとに集計） https://kaigo-souba.com/data/
```

- ブログ・ホームページ：表やグラフのすぐ下に貼る
- 資料・スライド・レポート：そのページの下の端か、最後の「参考資料」に書く
- SNS・動画：投稿文や概要欄の最後に書く
- 表を加工・グラフ化したとき：「出典：介護施設相場.comのデータをもとに作成 https://kaigo-souba.com/data/」と書く
- URL は行の最後に置き、前に空白を入れる（URL のすぐ後ろに文字やカッコを続けると、リンクが切れることがあります）

許可の連絡やお金は要りません。出典さえ書けば、仕事（商用）でも自由に使えます。

元のデータは、厚生労働省「[介護サービス情報公表システム](https://www.mhlw.go.jp/stf/kaigo-kouhyou_opendata.html)」から抽出したオープンデータ（CC BY）、厚生労働省「第9期介護保険事業計画期間における介護保険の第1号保険料」、総務省「住民基本台帳に基づく人口、人口動態及び世帯数」で、各府省の利用規約に基づき介護施設相場.com が集計・加工しています。厚生労働省・総務省が作成したものではありません。

---

## English

Long-term care facilities in Japan by **prefecture (47) and municipality (about 1,900)**: number of residential care facilities by type, reported capacity, operator types, home-care offices, long-term care insurance premiums, certification rate and elderly population. Aggregated by [kaigo-souba.com](https://kaigo-souba.com/) from MHLW open data (Long-term Care Service Information Publication System, CC BY), MHLW premium tables and MIC resident population statistics. Files are UTF-8 with BOM. License: CC BY 4.0 — please credit "kaigo-souba.com, based on MHLW and MIC open data: https://kaigo-souba.com/data/". Not produced by MHLW or MIC. Synced daily from https://kaigo-souba.com/data/.
