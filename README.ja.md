# 製品取扱説明書・組立説明イラストレーションガイド＆SVG レイアウトテンプレート

[English](./README.md) | [简体中文](./README.zh-CN.md) | 日本語

本リポジトリは、製品取扱説明書、フラットパック家具の組立ガイド、クイックスタートガイド（同梱リーフレット）、保守・メンテナンス手順書、および医療・機器向け添付文書／使用説明書（IFU）のためのオープンな設計仕様、実践的なレビューチェックリスト、ならびに編集可能な SVG レイアウトテンプレート集です。プロダクトマネージャー、テクニカルライター、インダストリアルデザイナーやドキュメントデザイナー向けに構築されており、複雑な手順を明確な 1 ステップ 1 アクションに分解し、視点、線幅、動作矢印、部品表（BOM）の引き出し線、安全警告を標準化し、任意のベクターエディタで白紙から作ることなく印刷・Web 対応の A4 / A5 ページを組版できます。ManualFig（ManualFig.ai）の公式サイトは [https://manualfig.ai/ja](https://manualfig.ai/ja) です。

---

## リポジトリ構成

```text
.
├── guide/
│   ├── en.md                              # Full illustration specification & QA checklist (English)
│   └── zh-CN.md                           # Full illustration specification & QA checklist (Simplified Chinese)
├── templates/
│   ├── single-step-a5-portrait.svg        # Single-step page (A5 portrait, 148 × 210 mm)
│   ├── four-grid-steps-a4-portrait.svg    # 2×2 four-panel step page (A4 portrait, 210 × 297 mm)
│   ├── exploded-view-bom-a4-portrait.svg  # Exploded view + BOM table page (A4 portrait, 210 × 297 mm)
│   └── safety-warnings-a5-portrait.svg    # Safety & warnings comparison page (A5 portrait, 148 × 210 mm)
└── examples/
    ├── README.md                          # Breakdown of how each finished example applies the guide
    ├── result-furniture-assembly.webp     # 6-step wordless bookshelf assembly & anti-tip check
    ├── result-appliance-filter.webp       # 4-step water purifier filter replacement & leak check
    ├── result-electronics-sim.webp        # 5-step SIM tray quick-start & orientation check
    ├── result-industrial-maintenance.webp # 4-step equipment lockout/tagout & lubrication SOP
    ├── result-stroller-safety.webp        # 4-step stroller unfolding, harness fit & brake check
    └── result-medical-ifu.webp            # 4-step wearable sensor patch application IFU
```

---

## イラストレーションガイドの収録内容

完全な仕様については [`guide/en.md`](./guide/en.md)（または中国語版の [`guide/zh-CN.md`](./guide/zh-CN.md)）を参照してください。

| セクション | 主なポイント |
|---------|---------------|
| [1. ステップ分解の原則](./guide/en.md#1-step-decomposition-principles-one-action-per-step) | 番号付きの各パネルを**1 つの主要な物理アクション**に限定し、同一の反復締結部品はまとめ（`A ×4`）、異なる動作は分割し、完了状態の視覚的手がかりを示します。 |
| [2. 視点の選択](./guide/en.md#2-viewpoint-selection-isometric-exploded-detail-callouts) | 連続するステップ間でアイソメトリック（等角投影）のカメラ角度を統一し、面一や対称性の確認には正投影図へ切り替え、`3–4 mm` 未満の細部には `2×–4×` の拡大図を追加します。 |
| [3. 線幅と視覚的階層](./guide/en.md#3-line-weights--visual-hierarchy) | 4 段階の線幅階層（外周輪郭 `1.4–2.0 pt`、内部の折り目・稜線 `0.75–1.0 pt`、引き出し線・軸線 `0.40–0.55 pt`）を用い、`0.35 pt` 以上を維持し、線の交差部には白フチの隙間（ホワイトハロー）を設けます。 |
| [4. 矢印と動作表現](./guide/en.md#4-arrows--motion-representation) | 太い動作矢印、黒丸付きの引き出し線、破線の分解軸線を視覚的に区別し、回転リボン矢印は軸の周囲に巻き付けて 3D の回転方向が一目で分かるようにします。 |
| [5. 部品番号と BOM の対応](./guide/en.md#5-part-numbering--bill-of-materials-bom-mapping) | マスター BOM、金具袋、各ステップの締結部品ボックス全体で部品 ID を一貫させ、外周の部品バルーンは引き出し線が交差しないよう整列配置します。 |
| [6. ワードレス（無文字）設計](./guide/en.md#6-wordless-instruction-design) | 組立前の工具・人数ストリップ、部品の非対称性の強調、`✓` と `✗` の向き比較ペア、ロック・チェック記号を組み合わせ、レビュー時にはキャプションを隠して理解度を検証します。 |
| [7. 警告・安全情報の提示](./guide/en.md#7-presenting-warnings-cautions--safety-information) | 危険が生じる該当ステップのパネル上に直接安全上の注意を配置し、色による区別には必ず `✓` / `✗` 記号を併用し、対象市場の適用規格に照らして記号と文言を確認します。 |
| [8. 多言語レイアウト](./guide/en.md#8-multilingual-layout--localization-considerations) | 翻訳対象テキストを線画から分離し、文字数が増える言語向けに `35%–50%` の余白を確保し、RTL（右から左）言語ではパネル順序のみを反転させ、ねじ向きや製品の物理形状は決して反転させません。 |
| [9. 書き出し形式の選択](./guide/en.md#9-export-format-selection-svg--pdf--png) | Web やベクター受け渡しには明示的な `viewBox` を持つ SVG、印刷冊子には `100% K` のベクター PDF、ダークモードで線が見えなくなるのを防ぐには `300–600 DPI` の白背景 PNG を使用します。 |

---

## すぐに編集できる SVG ページテンプレート

[`templates/`](./templates/) 内の 4 つのファイルはすべて、正確な A4 / A5 比率（`4 SVG units = 1 mm`）、意味構造に沿った `<g id="...">` レイヤーグループ、白ベタ `#FFFFFF` のページ背景、および汎用システムサンセリフフォントスタックを用いた、手書きかつ外部依存なしの SVG 1.1 XML ドキュメントです。

| テンプレートファイル | 物理サイズ | `viewBox` | 含まれるレイアウトモジュール |
|---------------|---------------|-----------|-------------------------|
| [`single-step-a5-portrait.svg`](./templates/single-step-a5-portrait.svg) | A5 縦（`148 × 210 mm`） | `0 0 592 840` | ランニングヘッダー、ステップバッジ、ステップ別の金具コールアウト枠、メインのアイソメ図プレースホルダー、`3×` 拡大鏡サークル、完了確認インセット、多言語対応キャプション枠、動作凡例。 |
| [`four-grid-steps-a4-portrait.svg`](./templates/four-grid-steps-a4-portrait.svg) | A4 縦（`210 × 297 mm`） | `0 0 840 1188` | セクションヘッダー、組立前の工具・人数・マット表示ストリップ、`2×2` の番号付きステップカード（`1`–`4`）、ミニ金具枠、`✓`/`✗` ペア、`180°` 反転記号、リスク発生箇所の耐荷重ボックス、フッター凡例。 |
| [`exploded-view-bom-a4-portrait.svg`](./templates/exploded-view-bom-a4-portrait.svg) | A4 縦（`210 × 297 mm`） | `0 0 840 1188` | 分解図キャンバス、同軸破線トレースライン、交差しない整列済み部品バルーン（`1`–`6`）、実寸 `1:1` の 50 mm 金具スケール目盛り、5 列の BOM テーブル（`Item`、`Part No.`、`Part Name`、`Spec`、`Qty`）。 |
| [`safety-warnings-a5-portrait.svg`](./templates/safety-warnings-a5-portrait.svg) | A5 縦（`148 × 210 mm`） | `0 0 592 840` | 構造化された警告バナー（危険源、結果、回避方法）、注意ブロック、誤（`✗`）と正（`✓`）の並列状態プレースホルダー、使用前安全チェックリスト。 |

### テンプレートを単体で使う方法（専用ツール不要）

1. **任意のベクターエディタで開く**：Inkscape（無料・オープンソース）、Figma、Adobe Illustrator、Affinity Designer、または CorelDRAW で `.svg` ファイルを読み込みます。物理的な `mm` 寸法により、自動的に実寸 100% の印刷スケールで開きます。
2. **プレースホルダー領域を製品イラストに差し替える**：破線の `<rect class="placeholder-zone">` または `<g id="exploded-part-placeholders">` グループを見つけ、手元のベクター線画やトレースした CAD ビューを配置してから、プレースホルダーの矩形を削除します。
3. **コールアウトとキャプションを更新する**：`<text>` 要素からステップタイトル、金具の数量（`A ×4`）、BOM の各行を直接編集します。マニュアルを他言語へ翻訳する予定がある場合は、キャプション枠内の下部余白を残しておきます。
4. **安全マージンガイドを非表示にして書き出す**：`<rect id="safe-margin-guide">` を非表示または削除し、[10 項目のチェックリスト](./guide/en.md#10-pre-release-quality-checklist) に照らして確認したうえで、印刷用 PDF、クリーンな SVG、または白背景 PNG として書き出します。

---

## 注釈付き作例（Annotated Examples）

[`examples/README.md`](./examples/README.md) では、ワードレスのフラットパック本棚組立・転倒防止確認、浄水器フィルター交換、SIM カードのクイックスタート、産業機器のロックアウト／タグアウト・注油手順、ベビーカーの安全確認、ウェアラブル医療センサーパッチの IFU という 6 つの完成作例について、本仕様の各ルールがどのように適用されているかを視覚的に解説しています。

---

## 自動化したい場合

すべてのパネルを一から手描きする代わりに既存の製品資料から説明書イラストを作成したい場合、[ManualFig](https://manualfig.ai/ja) は製品写真、CAD スクリーンショット、スケッチ、既存の説明書ページ、およびテキストプロンプト（PNG、JPEG、WebP のアップロードに対応、1 回の実行につき 4 MB 未満の参照画像を最大 3 枚まで）から、クリーンな線画、組立ステップ図、IFU パネル、および線編集可能なストロークベースの SVG または PNG 図版を生成します。キャンバス上での確認、テキスト編集、プロジェクト履歴機能を備えており、新規登録時に 10 クレジット、さらに毎日 10 クレジットの無料枠が付与されます（デフォルトでは画像または SVG の生成 1 回につき 10 クレジット消費）。なお、生成されるイラストは説明文書向けの補助ビジュアルであり、認証済みの設計図面、規制当局への提出書類、または認証済み安全文書に代わるものではありません。

- 公式サイト（日本語）：[https://manualfig.ai/ja](https://manualfig.ai/ja) · 英語版：[https://manualfig.ai](https://manualfig.ai)
- ツール選定ガイド：[製品取扱説明書イラスト作成ソフト比較](https://manualfig.ai/ja/blog/product-manual-illustration-software-comparison) · [AI 組立説明書・手順図作成ツール比較](https://manualfig.ai/ja/blog/ai-assembly-instruction-tools-comparison)

---

## ライセンス

- **コードおよび SVG テンプレートマークアップ**：MIT License
- **ドキュメントおよびサンプル画像**：Creative Commons Attribution 4.0 International (CC BY 4.0)
