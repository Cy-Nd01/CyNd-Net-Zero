# 05 — The OSI Model

---

## Why does this model even exist?

When a problem happens in a country, they don't write a new law for every single crime.
They already have a legal system they refer back to.

The OSI Model is exactly that — a reference model we go back to whenever we need
to describe or troubleshoot what's happening in a network.

Without it, every time someone asked "where's the problem?"
we'd have no common language to answer with.

---

## OSI vs TCP/IP

The OSI Model has 7 layers — but that's theoretical.
In real life, we use the **TCP/IP suite**, which has 4 layers.

OSI = the reference. TCP/IP = what actually runs the internet.

---

## The 7 Layers — and how to never forget them

> **"Please Don't Throw Sausage Pizza Away"**

| # | Letter | Layer | What lives here |
|---|--------|-------|-----------------|
| 1 | P | Physical | Cables, fiber, wireless (WiFi) |
| 2 | D | Data Link | MAC addresses, Frames, Trailer |
| 3 | N | Network | IP addresses, Packets |
| 4 | T | Transport | TCP/UDP, Segments, Sequence numbers |
| 5 | S | Session | Opens, manages, and closes your session |
| 6 | P | Presentation | Encryption/decryption (like WhatsApp) |
| 7 | A | Application | Protocols like HTTP, HTTPS — not the apps on your phone |

---

## Layer by layer

**Layer 1 — Physical**
The actual hardware. Three types:
- **Copper cables** — good for short distances
- **Fiber optic** — expensive, but better quality
- **Wireless** — WiFi

You can't hack this layer remotely — you'd have to be physically present.

**Layer 2 — Data Link**
Home of the MAC address. Data here is called **Frames**.
A Trailer is added — extra info at the end to catch any errors during unpacking.

**Layer 3 — Network**
Home of the IP address. Data here is called **Packets**.

**Layer 4 — Transport**
TCP and UDP live here. Data here is called **Segments**.
Sequence numbers are added so packets can be reassembled in the right order.

**Layer 5 — Session**
Creates, manages, and terminates your session.
Like when you open Chrome — something has to start that connection and end it.

**Layer 6 — Presentation**
Handles encryption and decryption.
Also makes sure the data reaches the right application in a format it understands.
Like WhatsApp — your messages are encrypted here before they leave your device.

**Layer 7 — Application**
Not the apps on your phone.
This is where network protocols like HTTP and HTTPS live —
the ones that actually deliver network services to you.

---

## One last thing

When you're working in cybersecurity and someone says
"Layer 4 issue" or "it's a Layer 7 problem" —
you won't be lost. You'll know exactly what they mean.

---

*Written in my own words — not copy-pasted.*
