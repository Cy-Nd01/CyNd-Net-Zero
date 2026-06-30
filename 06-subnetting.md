# 06 — Subnetting

---

## The part everyone dreads

You might be wondering what crime you committed to end up here.
Don't worry — by the end of this, it'll make sense.

---

## What is subnetting and why do we even need it?

Subnetting is what lets you look at something like /24 or /26 and immediately
know what it means — how many devices, how many networks, all of it.

But it's not just about solving problems on paper.
It's about understanding why we chose /24 over something else in the first place.

Imagine a company with 1020 developers and 40 HR employees.
Would you give everyone the same subnet?
Of course not. That's called **IP address waste** —
and IP waste is part of why we almost ran out of IPv4 addresses
and had to think about IPv6 in the first place.

---

## Why does subnetting matter beyond just the math?

Without subnetting, if you had 65,000 addresses in one flat network:
- Security would be a nightmare — more exposure, more attacks
- The network would be incredibly slow

Think of it like carrying a massive bundle of wood.
You can't move it all at once — you split it into smaller pieces.
Easier to carry, faster to move, nothing falls on the floor.

That's subnetting. Smaller networks = more security, better speed, zero waste.

---

## How do we know how many devices fit in a subnet?

Remember IPv4 is 32 bits.

Take /24 as an example:

32 - 24 = 8 bits left for hosts

2⁸ = 256

But don't fall for the trap — two addresses are always reserved:
- The first → **Network Address** (like the street name)
- The last → **Broadcast Address**

Think of it like a microbus — the first and last seats are always taken.

So the actual number of usable hosts = **254**

---

## CIDR Notation

The /24 is just a shortcut. Its full name is **CIDR Notation**
(Classless Inter-Domain Routing).

It tells you how many bits are reserved for the network.

**Rule to never forget:**
> The lower the CIDR number, the more hosts you can have.

---

## The Subnet Mask

The subnet mask works like a marker that tells you
where the street name ends and where the house number begins.

For /24:
- The first 24 bits = all 1s (network part)
- The remaining 8 bits = all 0s (host part)

Why 1s and 0s? Because computers only understand binary.

---

## How does a device know if another device is on the same network?

The device takes both IP addresses, converts them to binary,
and compares them bit by bit using something called an **AND gate** —
one of the logical gates in computing (others include OR, NOT, XOR).

AND gate rule:
- 1 AND 1 = 1
- 1 AND 0 = 0

If the result matches → same network → no routing needed.
If it doesn't match → different network → the data has to travel
across routers, oceans, and back — like sending a message
to a friend in America vs your brother next door.

---

## VLSM — giving each department what it actually needs

**VLSM (Variable Length Subnet Masking)** means
different parts of a company get different subnet sizes
based on how many devices they actually have.

Developers with 1022 devices get a bigger subnet.
HR with 40 devices gets a smaller one.

No waste. No over-allocating. Everyone gets exactly what they need.

---

## Reading the subnet mask in binary

When you see /24, that means the first 24 bits are 1s.

To convert: take each 1 and assign it a value from left to right:
128 → 64 → 32 → 16 → 8 → 4 → 2 → 1

Add up the 1s, ignore the 0s. That gives you the subnet mask.

And one thing to never forget:
> When working with subnets below /24, don't look at the last octet —
> look at the one before it.

---

## Wrapping up the Network Refresher

This is everything I covered in the networking fundamentals section.
I studied the basics, and I'm sharing what I learned — in my own words,
at my own level, as part of my journey.

If even one thing here made sense to you, that's enough for me.
I'll keep sharing as I go.

---

*Written in my own words — not copy-pasted.*
