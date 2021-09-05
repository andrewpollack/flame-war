## Description
Ever seen a thread on Reddit where two+ people are fighting in the comments? I have, and I've always been curious to visualize the depth of their conversations. No, not the depth-content, but the literal "how long are these people fighting...". 

This is where `flame-war` will come in handy! The idea is simple: you feed in a Reddit post URL, and receive a [flame graph](https://www.brendangregg.com/flamegraphs.html) output visualizing the stack of the comments.

## Motivation
I love flame graphs. Since starting to use them for profiling CPUs, I've been curious to see other mediums they can be used in. Additionally, I've been wanting to practice more writing code in [Rust🦀](https://www.rust-lang.org/). So why not combine both into one fun project?

## Timeline/Strategy
- Finish implementing [`perf` flame graph implementation in Rust](https://github.com/andrewpollack/blaze)
    - Helps form baseline of flame graph generation
- Investigate [Reddit API](https://www.reddit.com/dev/api/) to formulate way to convert URL --> information about comments
- Craft desired flame graph output
    - What to give as flame graph names?
    - How to resolve depth that is too far for dev API?
- Output flame graph in SVG

--- Future stretch goals ---
- Create web-app to allow user to enter URL, and immediately get SVG in browser
    - Requires looking into Rust web-app libraries... will be interesting!
- Implement simplified key --> value caching layer (Redis) to save on computation
- Implement CI/CD on project
    - Practices implementing CI/CD from scratch