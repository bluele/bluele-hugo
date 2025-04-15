---
title: "about"
date: 2025-04-15T00:00:00+09:00
draft: false
---

I'm a hacker and entrepreneur. I specialize in abstracting complex problems and building frameworks and middleware to solve them. My expertise spans from developing cutting-edge technologies to applying them in real-world products that address practical challenges.

## Professional Experience

### Datachain (2018–Present): Co-founder, CTO, Research Engineer

- Leading research and development in blockchain interoperability, with a particular focus on IBC, light client algorithms, and middleware enabling cost-effective on-chain light client verification
- Supporting the development of [TOKI](https://toki.finance/), a cross-chain token transfer protocol, by providing core infrastructure and technical design based on IBC and LCP
- Designing and developing PoCs in collaboration with partner companies (e.g., Progmat, MUTB, Toyota Financial Services, NTT DATA, etc.)
- See the “Media” section for notable project coverage

Representative projects include:

- [LCP](https://github.com/datachainlab/lcp): A proxy middleware that enables light client verification using Trusted Execution Environments (TEE)
- [zkDCAP](https://github.com/datachainlab/zkdcap): A zero-knowledge proof-based Intel SGX DCAP quote verification system
- [Hyperledger YUI](https://github.com/hyperledger-labs/?q=yui-): An implementation of the IBC (Inter-Blockchain Communication) protocol for Ethereum and other enterprise blockchains
- [Cross Framework](https://github.com/datachainlab/cross): A framework for building smart contracts that support cross-chain transactions via IBC
- [Hypermint](https://github.com/datachainlab/hypermint): A Tendermint-based blockchain supporting WASM smart contracts
- Ethereum L2 Plasma chain: Developed using Solidity, Golang, and Tendermint

### Freelance: Lead Engineer

Worked on backend systems in the adtech industry, primarily focused on building and scaling infrastructure to handle high-traffic environments.

- High-performance ad server (>100,000 RPS): Built with Golang, Aerospike, AWS, Jenkins, Ansible, etc.
- Large-scale ad log batch processing: Implemented with Golang, Fluentd, and [go-flow](https://github.com/bluele/go-flow)

### Momentum (2014–2017): Co-founder, CTO

Developed and launched an ad verification service to protect advertisers from brand risk. Successfully integrated the service with DSPs and ad networks.

- Ad verification platform (brand safety, ad fraud detection): Go, JavaScript, Python, AWS, GCP (BigQuery)
- Designed a batch system capable of crawling tens of millions of URLs per hour
- Built a content classification system in collaboration with a laboratory at Tokyo Institute of Technology
- [Acquired by a KDDI Group company](https://jp.techcrunch.com/2017/07/26/syndot-momentum/)

### JustSystems (2013): Software Engineer

- Built backend systems for an ecommerce: Java, Scala, Play Framework, PostgreSQL, Redis, AWS
- Conducted research and development on similar-image retrieval systems as an experimental project: Python, OpenCV, Apache Solr

## Open Source (As Founder)

The following are projects I initiated. For additional contributions, please visit my GitHub: https://github.com/bluele

- [gcache](https://github.com/bluele/gcache): In-memory cache library supporting various eviction strategies; [widely adopted](https://github.com/search?l=&o=desc&q=github.com%2Fbluele%2Fgcache+language%3AGo&s=indexed&type=Code)
- [hypermint](https://github.com/datachainlab/hypermint): WASM-compatible blockchain built on Tendermint
- [redis-semaphore](https://github.com/bluele/redis-semaphore): Distributed semaphore and mutex implementation using Redis
- [factory-go](https://github.com/bluele/factory-go): A factory pattern library for setting up Golang objects
- [More on GitHub](https://github.com/bluele?tab=repositories)

## Technical Skills

- **Programming Languages**: Rust, Go, C, Python, JavaScript
- **Confidential Computing**: Intel SGX
- **Databases**: MySQL, Redis, Aerospike
- **Blockchain**: Ethereum, Tendermint, Cosmos-SDK, IBC
- **Cloud Platforms**: AWS, Azure, GCP

## Media Coverage

- [An introduction of ZK-IBC implementation](https://ibcprotocol.dev/blog/zkibc-toki)
- [Meet YUI, a Hyperledger Lab tackling cross-chain and off-chain challenges](https://www.hyperledger.org/blog/2021/06/09/meet-yui-one-the-new-hyperledger-labs-projects-taking-on-cross-chain-and-off-chain-operations)
- [Cross Framework featured in Nikkei xTECH](https://xtech.nikkei.com/atcl/nxt/column/18/00001/04861/)
- [Hypermint used in a PoC with Toyota Financial Services](https://prtimes.jp/main/html/rd/p/000000001.000055051.html)
