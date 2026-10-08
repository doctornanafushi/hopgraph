# HopGraph — 1-minute pitch script

**0:00-0:12**

Moving assets across chains is confusing. Bridges and DEXs all charge different, hidden fees. Users end up overpaying without knowing it.

> チェーン間で資産を移動するのは複雑です。ブリッジやDEXはそれぞれ異なる、見えにくい手数料を課しています。ユーザーは気づかないまま余分な費用を払っています。

**0:12-0:30**

HopGraph fixes this. We model chains, bridges, and DEXs as a weighted graph. Then we run Dijkstra and A star search to find the cheapest path, in real time.

> HopGraphはこれを解決します。チェーン、ブリッジ、DEXを重み付きグラフとしてモデル化します。そしてダイクストラ法とA*探索を使い、リアルタイムで最も安い経路を見つけます。

**0:30-0:48**

Here's how it works. You pick your source and destination. HopGraph pulls live fee, slippage, and gas data. It shows the top three cheapest routes, then executes with one click, using Wormhole, deBridge, and Jupiter.

> 仕組みはこうです。送信元と送信先を選びます。HopGraphはリアルタイムの手数料、スリッページ、ガス代データを取得します。最も安い上位3つの経路を表示し、ワンクリックでWormhole、deBridge、Jupiterを使って実行します。

**0:48-1:00**

Liquidity is now fragmented across dozens of chains. Manual comparison doesn't scale anymore. HopGraph turns that chaos into one simple, optimal route. Next, we're adding more bridges and an LP rebalancing mode.

> 流動性は今や何十ものチェーンに分散しています。手動での比較はもはやスケールしません。HopGraphはその混乱を、ひとつのシンプルで最適な経路に変えます。次は、より多くのブリッジの追加と、LP向けリバランスモードを計画しています。
