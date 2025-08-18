+++
title = '2025-08-18: The Hidden Cost of Cheap Components'
date = 2025-08-18T20:00:00+02:00
draft = false
[params]
  author = 'Magnus Nordlander'
+++
There's a persistent attitude in the maker community that hardware problems can probably be solved with clever software. It's an attractive proposition – software is free to iterate on, endlessly flexible, and doesn't require waiting for shipping or spending more money. But sometimes, this mindset leads us down expensive rabbit holes when the real problem is simply that we're using components that aren't up to the task.

### The Software Trap

When faced with unreliable hardware behavior, the modern engineer's first instinct is often to reach for a software solution. It makes sense – we're more comfortable with code than with swapping components, and software fixes feel more elegant, more "engineered." We implement debouncing algorithms, add filtering, try interrupt-driven approaches, even deploy dedicated hardware peripherals like PIOs to handle timing-critical tasks.

This approach isn't wrong, per se. Many hardware issues *can* be mitigated in software. Contact bounce is real, timing issues exist, and clever code can often work around these limitations. But there's a critical question we often fail to ask: should we be working around these issues at all?

### The Quality Paradox

The maker community has been blessed (and cursed) with an abundance of cheap components from overseas manufacturers. A rotary encoder module for $2? A complete sensor board for $5? It seems foolish to pay 5-10x more for a "name brand" component when the cheap alternative appears to do the same thing.

But here's what the spec sheets don't tell you: cheap components often come with hidden costs. They might work... most of the time. They might be reliable... under ideal conditions. They might last... for a while. The problems manifest in subtle ways – spurious readings, intermittent failures, degradation over time. Issues that send you diving into your code, questioning your implementation, doubting your design choices.

### A Case in Point

Consider the humble rotary encoder – a seemingly simple component that translates rotation into digital signals. The cheap KY-040 modules flooding the market use unknown encoders of questionable providence. They're clones of clones, built to hit a price point rather than a quality standard. 

In contrast, a genuine Bourns PEC11R – the component many of these cheap encoders attempt to copy – costs significantly more but delivers exactly what it promises. Same footprint, same basic function, but the difference in reliability is night and day. What seems like a $10 savings becomes days of debugging, multiple iterations of software "fixes," and ultimately, the cost of buying the quality component anyway.

### The True Economics

Let's do the math that we often avoid. If you value your time at even a modest $50/hour, spending just two hours debugging a cheap component has already cost you $100 in time – far more than the price difference between the cheap and quality part. Add in the frustration, the delayed project timeline, and the potential for field failures if you're building something others will use, and the "savings" evaporate entirely.

This calculation becomes even more stark for professional engineers or anyone building products for others. The reputation cost of unreliable hardware, the support burden of field failures, and the opportunity cost of time spent on preventable problems can be devastating.

### Where to Draw the Line

This isn't an argument for always buying the most expensive components. There are places where cheap parts make perfect sense – prototyping, non-critical applications, or when you're genuinely unsure about your design. The skill lies in knowing where quality matters.

Critical user interface elements? Invest in quality. Timing-sensitive components? Don't cheap out. Anything that will be hard to access once installed? Buy the best you can afford. Components that will see heavy use? Factor in the total lifecycle cost, not just the purchase price. Safety critical? *Definitely* get the good stuff.

### The mark of a professional engineer

One of the marks of a professional engineer is knowing where you can cut corners and where you can't. This knowledge comes from experience – often painful experience. But it's also something the maker community needs to discuss more openly. We either celebrate ingenuity and frugality, or we go all in and use *only* over-specced components. We don't talk enough about the false economy of cheap components, and we don't put enough effort into spreading the knowledge of where cutting corners are fine.

The proliferation of cheap components has democratized hardware development in wonderful ways, but we need to get better at finding the right balance of price and quality. Personally, I'm by no means a good example. I rarely find the right balance, either skimping out to save a couple of dollars, or picking precision name-brand resistors over cheap generics, because they *might* be necessary.

### Closing Thoughts

The next time you find yourself deep in a debugging session, trying to software your way around a hardware problem, take a step back. Ask yourself: is this a problem worth solving, or is it a problem worth avoiding? Sometimes, the answer is to open your wallet a little wider and buy the component that actually works.

Quality components aren't just about reliability – they're about respecting your time, maintaining your sanity, and building things that last. As someone concerned with sustainability and reducing electronic waste, choosing components that won't need replacement or cause entire projects to be scrapped is the responsible choice.

The most expensive component in any project is often the builder's time. Don't forget to factor that in to your consideration.