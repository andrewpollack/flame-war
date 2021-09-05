## Description ✍
Ever seen a thread on Reddit where two+ people are fighting in the comments? I have, and I've always been curious to visualize the depth of their conversations. No, not the depth-content, but the literal "how long are these people fighting...". 

This is where `flame-war` comes in handy! The idea is simple: you feed in a Reddit post URL, and receive a [flame graph](https://www.brendangregg.com/flamegraphs.html) visualizing the stack of the comments.

**Note:** For [crate.io](https://crates.io/crates/flame-war), the fully implemented version will begin with the **1.0** release. Until then, I hope you enjoy the process 😊

## Motivation 💪
I love flame graphs. Since starting to use them for profiling CPUs, I've been curious to see other mediums they can be used in. Additionally, I've been wanting to practice more writing code in [Rust🦀](https://www.rust-lang.org/), as well as work on my general SWE practices. So why not combine all into one fun project?

## Timeline/Strategy 🔃
- Finish implementing [`perf` flame graph implementation in Rust](https://github.com/andrewpollack/blaze)
    - Helps form baseline of flame graph generation
- Investigate [Reddit API](https://www.reddit.com/dev/api/) to formulate way to convert URL --> information about comments
- Craft desired flame graph output
    - What to give as flame graph names?
    - How to resolve depth that is too far for dev API?
- Output flame graph in SVG

--- Future stretch goals ---
- Create web-app to allow user to enter URL, and immediately get SVG in browser
    - *Requires looking into Rust web-app libraries... will be interesting!*
- Implement simplified key --> value caching layer (Redis) to save on computation
    - *Practices integrating Redis into Rust web-app stack*
- Robustify CI/CD on project
    - More tests
    - Github workflow to take most recent `main` push, and ensure tests run successfully
    - *Practices implementing CI/CD from scratch*
