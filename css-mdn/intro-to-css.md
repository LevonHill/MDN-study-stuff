<!-- @format -->

Introduction to the CSS cascade
The cascade is an algorithm that defines how user agents combine property values originating from different sources. The cascade defines the origin and layer that takes precedence when declarations in more than one origin, cascade layer, or @scope block set a value for a property on an element.

The cascade lies at the core of CSS, as emphasized by the name: Cascading Style Sheets. When a selector matches an element, the property value from the origin with the highest precedence gets applied, even if the selector from a lower precedence origin or layer has greater specificity.

This article explains what the cascade is and the order in which CSS declarations cascade, covering cascade layers and origin type. Understanding origin precedence is key to understanding the cascade.

(lets explain this deeply)
"When multiple CSS rules could apply to the same element, CSS must decide who wins.
That decision is done by an algorithm known as the cascade.

Think of it like a throne room full of declarations—
the strongest one rules.

But “strength” isn’t just specificity.
CSS looks at three major forces in this order:

1. ORIGIN PRECEDENCE — who the declaration comes from

There are 3 origins:

User Agent (browser defaults)

User styles (what the user sets in their browser)

Author styles (your CSS—this is usually the strongest)

Within these, there are also:

Normal rules

!important rules

So if conflicts exist:
author !important > user !important > author normal > user normal > user-agent

This is why !important demolishes other declarations.

2. CASCADE LAYERS — a newer rule structure

CSS now allows you to declare layers:

@layer reset;
@layer base;
@layer components;
@layer utilities;

Layers are like power tiers.
Layer priority is determined by the order you declare the layers, not specificity.

That means a rule in a higher-priority layer beats a rule in a lower-priority layer—even if the lower one is more specific.

Layers override specificity.
Understand this: a weak selector in a high layer beats a strong selector in a lower layer.

3. SPECIFICITY — selector strength

If two rules are from the same origin and the same layer, then CSS checks:

Inline styles (strongest)

ID selectors

Class / pseudo-class selectors

Tag selectors (weakest)

But remember:

Specificity ONLY matters after origin + layer are tied.

4. SOURCE ORDER — the final tie-breaker

If everything else ties (same origin, same layer, same specificity),
the rule written last in the CSS file wins.

This is the weakest but still real power.

🔥 The Key Insight You Missed

Your quote says:

“The origin with the highest precedence wins, even if the selector from the lower origin has greater specificity.”

Meaning:

@layer utilities {
.text-red { color: red; }
}

@layer base {
#title { color: blue; }
}

Even though #title has higher specificity (ID selector),
if utilities is a higher layer than base, then:

.text-red wins
because layer > specificity.

💀 Sukuna’s Final Lesson

CSS isn’t chaos.
It’s a structured system that determines which rule is strongest by:

Origin

Layer

Specificity

Order

Once you understand these levels, CSS becomes predictable and bendable to your will."
