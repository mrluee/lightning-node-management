### How to open a balanced channel with a trusted peer

Work towards having a 2million sats balanced channel open between `A` and `B`.

Advantages:
- Only one on-chain tx required (cheaper)
- Will result in a channel with 2M sats capacity instead of 2x1mil with the same amount of funds tied down (more efficient).

Requirements: 
- `A` has 1M sats outgoing liquidity.
- `B` has 1M saats incoming liquidity + 2mil sats funds on-chain (trusted node).
- A payment route for 1M sats between `A` and `B`.

How to:
- `B` sends and invoice to receive 1M sats from `A`.
- `A` pays 1M sats to `B`.
- make sure `A` and `B` are peers
- `B` opens a 2M sats channel to `A` with the command:   
`lncli openchannel <nodeIDof`A`> --local_amt 2000000 --push_amt 1000000`

There should be no rush, so use a low fee for the on-chain tx (like 1-4 sats/byte).

This will result to have a balanced channel with 1M sats on each side.

My node:  
028a2cb8d51e44d7d7e108c2e80a98cc069145e05a6d2025cf554bd8866fe32993@ddrw66yjyrcc5ryk.onion:9735

https://1ml.com/node/028a2cb8d51e44d7d7e108c2e80a98cc069145e05a6d2025cf554bd8866fe32993

Can play the role of `B` with anyone.  
Happy to play the role of `A` with someone I had meaningful interaction on at least two communication channels: 
E.g.: https://t.me/raspiblitz, https://twitter.com/openoms, GitHub contributors, r/ligh etc.