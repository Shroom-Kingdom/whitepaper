# Unique Selling Propositions

This chapter discusses several USPs, that make Shroom Kingdom unique and valuable.

## NEAR Protocol

Shroom Kingdom will be developed on NEAR Protocol, which is a Smart Contract capable layer-one blockchain.

NEAR Protocol wants to solve scaling issues of prior blockchains by introducing a sharded architecture.
With a block time of about 1 second and very low gas fees, transactions are both fast and cheap.
The sharding architecture makes sure, that these metrics won't change with an increasing amount of transactions.
NEAR Protocol is also
<a href="//near.org/blog/near-climate-neutral-product/" target="_blank" rel="noopener">
certified climate neutral{{#include icons/link.svg}}</a> by supporting green projects.
Another aspect about NEAR Protocol is its focus on User Experience,
which includes the smooth user onboarding process but also for developers the ease of use of building Web3 applications.

## Technology stack

The game itself will be a web application.
It runs in browsers via Rust compiled to WebAssembly and uses WebGL2 for rendering.

WebAssembly is a new binary format for the web, that has been available in all major browsers since 2018.
Ever since then it found its way into other environments like "regular" backends, serverless and blockchain.
The reason behind this is its built in portability and security.
WebAssembly is meant to be a common compilation target for many programming languages,
which makes it possible to allow cross language communication via
<a href="//hacks.mozilla.org/2019/08/webassembly-interface-types/" target="_blank" rel="noopener">
Interface Types{{#include icons/link.svg}}</a>.

NEAR Protocol also allows building Smart Contracts that compile to WebAssembly.
This approach of building Smart Contracts has the extreme advantage over other Smart Contract capable blockchains,
that developers have a choice of what programming language they want to use.
NEAR Protocol already allows building Smart Contracts with their
<a href="//github.com/near/near-sdk-rs" target="_blank" rel="noopener">Rust SDK{{#include icons/link.svg}}</a>
or <a href="//github.com/near/near-sdk-as" target="_blank" rel="noopener"
>AssemblyScript SDK{{#include icons/link.svg}}</a>.
Both these languages pioneer the WebAssembly format and are considered the best choice,
if you want to compile to WebAssembly.

The app will also be built as a Progressive Web App (PWA).
PWAs let you install web applications to your home screen and allow client side caching.
Depending on the platform, the process for this is slightly different and eventually
only specific browsers will be able to do so.
PWAs launch in full screen and will automatically be updated on a cache miss with the new version of the application.
The distribution of PWAs doesn't happen from centralized app stores, which fits into the idea of blockchain.

As backend technologies Shroom Kingdom will use
<a href="//workers.cloudflare.com" target="_blank" rel="noopener">CloudFlare Workers{{#include icons/link.svg}}</a>,
which is a serverless edge computing environment.
Edge computing is a terminology focused on bringing computing as close to the source of data as possible in
order to reduce latency and bandwidth use.
Serverless is a way of running stateless functions on a cloud server.
It is another abstraction layer above cloud computing and uses a pay-per-use model rather than having running server costs.
You also don't have to care about scaling your backend,
because serverless functions automatically scale with the amount of requests.
Other resources that the serverless functions depend on
can still become a bottleneck in the overall architecture of the application, e.g. the database.

## Gaming & earning

- familiar gaming characters
- play-to-earn with passive income
- free-to-play. No initial investment needed
