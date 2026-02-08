---
marp: true
style: |
  :root {
    --bg: #454552;
    --text: #d8e9ef;
    --accent: #4ea1d3;
    --accent-2: #e85a71;
  }
  section {
    background: var(--bg);
    color: var(--text);
    font-family: "Inter", "Hiragino Kaku Gothic ProN", "Noto Sans JP", sans-serif;
    letter-spacing: 0.02em;
    text-align: left;
    padding: 50px 60px 40px;
  }
  section:not(.lead) {
    display: flex !important;
    text-align: left !important;
    justify-content: flex-start !important;
    align-items: flex-start !important;
    flex-direction: column;
  }
  section:not(.lead) > * {
    margin-left: 0 !important;
  }
  section.lead * {
    text-align: center !important;
  }
  section.lead {
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 0;
  }
  h1, h2 {
    color: var(--accent);
    font-weight: 700;
  }
  h3 {
    color: var(--text);
    font-weight: 700;
  }
  h1 { font-size: 2.2rem; }
  h2 { font-size: 1.8rem; }
  h3 { font-size: 1.4rem; }
   .accent { color: var(--accent); }
   strong,.accent-2 { color: var(--accent-2); }
  .lead-sub { font-size: 1.1rem; opacity: 0.9; color: var(--accent-2); }
  .card {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 14px;
    padding: 14px 16px;
  }
  .grid {
    display: grid;
    gap: 12px;
    width: 100%;
  }
  .grid-3 { grid-template-columns: repeat(3, 1fr); }
  .grid-2 { grid-template-columns: repeat(2, 1fr); }
  .grid-3 .card, .grid-2 .card {
    min-height: 120px;
  }
  .key-list {
    list-style: none;
    padding-left: 0;
  }
  .key-list li {
    margin-bottom: 12px;
  }
  .callout {
    border-left: 4px solid var(--accent);
    padding: 8px 12px;
    background: rgba(255,255,255,0.05);
    border-radius: 8px;
  }
  .flow-line {
    display: flex;
    gap: 10px;
    align-items: center;
    flex-wrap: wrap;
    margin-bottom: 8px;
  }
  .flow-line .step {
    background: rgba(255,255,255,0.08);
    border-radius: 999px;
    padding: 6px 12px;
    border: 1px dashed rgba(255,255,255,0.2);
  }
  .flow-blocks {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 18px;
    width: 100%;
    margin: 8px 0 14px;
  }
  .flow-block {
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.18);
    border-radius: 16px;
    padding: 18px 16px;
    text-align: center;
    font-size: 1.1rem;
    font-weight: 600;
    box-shadow: 0 6px 18px rgba(0,0,0,0.2);
  }
  .flow-block .label {
    display: block;
    font-size: 0.8rem;
    opacity: 0.7;
    margin-bottom: 6px;
  }
  .flow-block .sub {
    display: block;
    margin-top: 8px;
    font-size: 0.85rem;
    font-weight: 400;
    opacity: 0.75;
    line-height: 1.3;
  }
  .rag-flow {
    display: flex;
    flex-direction: column;
    gap: 18px;
    width: 100%;
    margin-top: 16px;
  }
  .rag-row {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 10px;
  }
  .rag-node {
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.2);
    border-radius: 14px;
    padding: 8px 14px;
    font-weight: 600;
    box-shadow: 0 4px 12px rgba(0,0,0,0.18);
  }
  .rag-node.subtle {
    font-weight: 500;
    opacity: 0.85;
  }
  .rag-arrow {
    color: var(--accent);
    font-weight: 700;
  }
  .rag-store {
    background: rgba(78,161,211,0.18);
    border-color: rgba(78,161,211,0.5);
  }
  .content-bottom {
    margin-top: 60px;
  }
  .merge-arrow {
    width: 100%;
    text-align: center;
    font-size: 2rem;
    color: var(--accent);
    margin: 10px 0 6px;
  }
  .hybrid-slide .card {
    padding: 10px 12px;
  }
  .hybrid-slide ul {
    font-size: 0.95rem;
    line-height: 1.35;
    margin: 6px 0 0;
  }
  .hybrid-slide h3 {
    font-size: 1.2rem;
    margin-bottom: 6px;
  }
  .hybrid-stack {
    width: 100%;
  }
  .arrow { color: var(--accent); font-weight: 700; }
  .chip {
    display: inline-block;
    padding: 2px 8px;
    border-radius: 999px;
    background: rgba(78,161,211,0.18);
    color: var(--accent);
    font-size: 0.85rem;
  }
  .badge {
    display: inline-block;
    padding: 2px 8px;
    border-radius: 6px;
    background: rgba(232,90,113,0.2);
    color: var(--accent-2);
    font-size: 0.85rem;
  }
  .checklist li { margin-bottom: 8px; }
  .checklist li::marker { color: var(--accent); }

  /* --- Code blocks (override Marp default theme) --- */
  section :is(pre, marp-pre) {
    background: rgba(0, 0, 0, 0.28) !important;
    border: 1px solid rgba(255, 255, 255, 0.14) !important;
    border-radius: 14px !important;
    padding: 18px 20px !important;
    box-shadow: 0 8px 22px rgba(0, 0, 0, 0.22);
    line-height: 1.35 !important;
    overflow: hidden !important;
    width: 100%;
    margin-top: 14px;
  }
  section :is(pre, marp-pre) code {
    /* Marp default theme uses 12px fixed -> too small. Override with scalable size. */
    font-size: 1.05rem !important;
    color: var(--text) !important;
    background: transparent !important;
    padding: 0 !important;
    white-space: pre-wrap;
    word-break: break-word;
  }
  section code {
    /* inline code */
    font-size: 0.95em;
    background: rgba(0, 0, 0, 0.18);
    border: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: 8px;
    padding: 0.08em 0.35em;
  }
---

<!-- _class: lead -->
# RAG入門

---
# RAGが生まれた理由
- LLMは学習時の知識と、プロンプトで与えられた情報しか扱えない
- 未学習の社内データや最新情報を活用したい
- すべての情報を事前にプロンプトへ詰め込むのは不可能
- そこで、質問を検索クエリにして文書を取得し、コンテキストに追加する発想がRAG

---
# RAGの構成要素
<div class="grid grid-2">
  <div class="card">
    <h3><span class="chip">① Retrieve</span></h3>
    <ul>
      <li>データ検索</li>
      <ul>
        <li>ベクトル検索</li>
        <li>テキスト検索</li>
        <li>ハイブリッド検索</li>
      </ul>
    </ul>
  </div>
  <div class="card">
    <h3><span class="chip">② Generate</span></h3>
    <ul>
      <li>LLMで回答生成</li>
      <ul>
        <li>プロンプトエンジニアリング</li>
        <li>コンテキストエンジニアリング</li>
      </ul>
    </ul>
  </div>
</div>

---
# Embedding
- テキストを意味空間のベクトルに変換する仕組み
- 手法はいろいろ
  - 単語頻度などの統計的手法
  - 機械学習によるベクトル化
- 現在は機械学習（深層学習）が主流

---
# ベクトル検索
<div class="flow-blocks">
    <div class="flow-block">
        <span class="label">Step 1</span>
        文書をEmbedding
    </div>
    <div class="flow-block">
        <span class="label">Step 2</span>
        クエリをEmbedding
    </div>
    <div class="flow-block">
        <span class="label">Step 3</span>
        近傍文書を取得
    </div>
</div>

<ul class="content-bottom">
  <li>ベクトルが高次元ほど<span class="accent-2">精度↑／コスト↑</span></li>
  <li>step3のアルゴリズムは色々ある</li>
  <ul>
    <li>HNSW</li>
    <li>IVF</li>
  </ul>
</ul>

---
# 一番シンプルなRAG構成
![bg](./rag-simple2.png)

---
# generatorのプロンプト例
```
関連する情報をもとに、質問に答えてください。

# 質問
{user_query}

# 関連情報
## document1
{document1}
## document2
{document2}
```

---
# なぜうまくいかないのか
- ドキュメントが長いと文脈が混在しやすい
- 混在した文脈は、ベクトル検索だけでは分離が難しい
  - AND、ORみたいな検索がベクトル検索は苦手
- 現実的な次元数では表現力が不足することが多い
  - 数学的に証明されている
 

---
# チャンキング
- ドキュメントを扱いやすいサイズに分割すること
  - 分割サイズ
  - どこで区切るか（段落/セクション）
- embeddingのベクトルの次元数も関係してくる
- 正解はなく、目的に合わせてチューニングが必要

---
# ハイブリッド検索
<div class="hybrid-slide">
  <div class="hybrid-stack">
    <div class="grid grid-2">
      <div class="card">
        <h3>ベクトル検索</h3>
        <ul>
          <li>意味の近さに強い</li>
          <li>表現ゆれに強い</li>
        </ul>
      </div>
      <div class="card">
        <h3>テキスト検索</h3>
        <ul>
          <li>キーワード一致に強い</li>
        </ul>
      </div>
    </div>
    <div class="merge-arrow">↓</div>
    <div class="card">
      <h3>ハイブリッド検索</h3>
      <div class="grid grid-2">
        <div>
          <ul>
            <li>ベクトル検索とテキスト検索を併用</li>
          </ul>
        </div>
        <div>
          <ul>
            <li>キーワードが含まれていて、内容も一致するものを取得</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

---
# リランキング
- 異なる2つの検索結果をマージし、ソートする必要がある
- 代表的アルゴリズムはRRF
  - 両方で上位に来る文書を高く評価する発想
- AIにマージソートさせる手法もあるがコスト大

---
# ちょっと凝ったRAG構成
![bg](./rag-full2.png)

---
# 検索を整えてもなぜうまくいかないのか
- リランキングやハイブリッド検索でも改善しきれないことがある
- 元データの品質が重要
  - 古い・誤ったデータがあるとコンテキストが汚染される
  - LLMが混乱し、誤答につながる
- 検索のチューニングと同じくらいデータ整備が重要

---
# まとめ
<ul class="checklist">
  <li>RAGは検索で文脈を補う仕組み</li>
  <li>成功の鍵はチャンキングと検索・リランキングの最適化</li>
  <li>そして<strong>高品質な元データ</strong>が不可欠</li>
</ul>
