# HopGraph

_Find the cheapest cross-chain path with real-time graph search, not guesswork_

## Summary

HopGraph models bridges, DEXs, and chains as a weighted graph and runs Dijkstra/A* search to find the lowest-total-cost route for moving or swapping assets across chains. It aggregates live fee, slippage, and gas data from multiple bridges and routers to recommend an optimal multi-hop path in real time. Both casual users and LPs get a single interface to execute the cheapest route instead of manually comparing bridges.

## Target users

DeFi users moving assets cross-chain and LPs rebalancing capital across chains

## Problem

Cross-chain transfers involve many bridges and DEXs with wildly different and opaque fee structures, making it hard to find the cheapest route manually.

## Solution

A pathfinding engine that treats the multi-chain DeFi landscape as a graph and continuously searches for the lowest-cost route using live fee/slippage data.

## MVP features

- Graph model of chains/bridges/DEXs with live-updated edge weights (fee, slippage, gas, time)
- Dijkstra/A* based route search returning top-3 cheapest paths
- One-click execution of the chosen route via integrated bridge/DEX SDKs
- Cost comparison dashboard showing savings vs naive single-bridge route
- Solana-first demo with 2-3 bridges (Wormhole, deBridge) and Jupiter for swaps

## Chains

Solana, Ethereum, Arbitrum, Base

## Tech

TypeScript, Rust, Dijkstra/A* pathfinding, Wormhole SDK, deBridge API, Jupiter Aggregator, The Graph/subgraph indexing

## Category

DeFi

## Why now

Liquidity and bridges have fragmented across dozens of chains and L2s, so manual fee comparison no longer scales and users are overpaying every day.

## Roadmap

- Add more bridges/DEXs and automated edge-weight refresh via oracles
- Build LP-specific rebalancing mode with impermanent loss modeling
- Launch as public API/widget for wallets and dApps to embed
