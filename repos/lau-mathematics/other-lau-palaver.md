# lau-palaver

## Intention

Consensus protocol inspired by the West African palaver tree. Communities make decisions through extended discussion until EVERYONE agrees. Not majority vote. Not weighted vote. Consensus or we keep talking.

## How It Works

Under the palaver tree, there is no deadline. The group discusses until every voice is heard and every objection is addressed. This crate implements that:
- **Palaver sessions:** open discussions where every participant can speak
- **Consensus detection:** not "most people agree" — everyone agrees or we keep going
- **Objection tracking:** every dissent is recorded, not dismissed
- **Timeout tolerance:** palaver trees have no clocks — the process takes as long as it takes
- **Resolution:** when consensus is reached, it's durable because everyone was heard
The insight: consensus is slow, but consensus is stable. A decision everyone agreed to doesn't need enforcement.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Consensus protocol inspired by the West African palaver tree. Communities make decisions through extended discussion until EVERYONE agrees. Not majority vote. Not weighted vote. Consensus or we keep t

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (38 lines), includes examples.

- README length: 55 lines, 2106 characters
- Documented sections: The concept in 60 seconds, Quick start, Key types

## Honest Assessment

Part of the sprawling Lau/PLATO ecosystem. The README covers basics but the project is one of many math/computation crates in this organization. The breadth of repos in SuperInstance (hundreds) raises questions about depth vs. breadth — many appear to be auto-generated or lightly documented. **This crate likely works as a component but standalone value is limited without the broader ecosystem.**
