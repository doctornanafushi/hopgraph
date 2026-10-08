# HopGraph
![HopGraph logo](assets/logo.png)

**Find the cheapest cross-chain path with real-time graph search, not guesswork**

## Overview

HopGraph is a cross-chain routing engine for DeFi. It models chains, bridges, and DEXs as a weighted graph and runs Dijkstra/A* pathfinding to find the lowest-total-cost route for moving or swapping assets across chains, using live fee, slippage, and gas data instead of guesswork.

## Problem

Cross-chain transfers involve many bridges and DEXs with wildly different and opaque fee structures. Comparing them manually is slow, confusing, and error-prone, so users and LPs routinely overpay without realizing it.

## Solution

HopGraph treats the multi-chain DeFi landscape as a graph: chains and assets are nodes, bridges and DEX routes are edges weighted by live fee, slippage, gas, and time data. A Dijkstra/A* search continuously finds the optimal multi-hop path, and users execute the chosen route in one click.

## Features (MVP)

- Graph model of chains/bridges/DEXs with live-updated edge weights (fee, slippage, gas, time)
- Dijkstra/A* based route search returning top-3 cheapest paths
- One-click execution of the chosen route via integrated bridge/DEX SDKs
- Cost comparison dashboard showing savings vs naive single-bridge route
- Solana-first demo with 2-3 bridges (Wormhole, deBridge) and Jupiter for swaps

## Tech Stack

TypeScript, Rust, Dijkstra/A* pathfinding, Wormhole SDK, deBridge API, Jupiter Aggregator, The Graph/subgraph indexing.

## How It Works

```
[User Input] -> [Graph Builder] -> [Dijkstra/A* Search] -> [Top-3 Routes]
                     ^                                         |
                     |                                         v
          [Live Fee/Slippage/Gas Feeds]           [One-Click Execution]
          (Wormhole, deBridge, Jupiter,                 |
           subgraph indexing)                             v
                                                [Wormhole / deBridge / Jupiter SDKs]
```

1. User selects source chain, destination chain, and asset.
2. HopGraph builds/updates the graph with live edge weights from bridges and DEXs.
3. Dijkstra/A* search computes the top-3 cheapest paths.
4. User picks a path; HopGraph executes it via the relevant bridge/DEX SDKs.
5. A dashboard shows the route and savings versus a naive single-bridge route.

## Roadmap

- Add more bridges/DEXs and automated edge-weight refresh via oracles
- Build an LP-specific rebalancing mode with impermanent loss modeling
- Launch as a public API/widget for wallets and dApps to embed

## Pitch

See the full pitch deck at [docs/pitch.pdf](docs/pitch.pdf) and the spoken script at [docs/pitch-script.md](docs/pitch-script.md).

## Team

- Name / role — placeholder
- Name / role — placeholder
- Name / role — placeholder

Built for the Colosseum hackathon (Solana and other chains).

---

🎬 Pitch video: [docs/pitch-video.mp4](docs/pitch-video.mp4)


## Prototype

Live prototype: https://doctornanafushi.github.io/hopgraph/

The source is [docs/index.html](docs/index.html) (served with GitHub Pages from the /docs folder). All data is simulated.
