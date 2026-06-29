# 01 — IP Addresses

Think of an IP address like your home address. Without it, no one knows where to send the data.

But before we even talk about IP addresses, where do they actually live? They live on **Layer 3 of the OSI Model** — the Network Layer.

---

## So why do we even need IP if we already have MAC?

MAC works fine — but only inside the same network. The moment you want to send data through a router to somewhere outside your network, MAC taps out. That's where IP comes in. IP is like telling someone your full location — not just your apartment, but the whole address.

---

## Two versions: IPv4 and IPv6

Yes, there are two versions. And no, they're not spells.

**IPv4** — 32-bit, gives us around 4 billion addresses. Sounds like a lot, right? People used to think it was impossible to run out. Then we got smartphones, laptops, tablets, smart TVs — and get this — fridges and washing machines with WiFi. Suddenly 4 billion wasn't enough. Big companies like Google and Apple bought huge blocks of IPs just for themselves. So yeah, we ran out.

**IPv6** — built to replace IPv4. 128-bit, practically unlimited addresses. But we're not fully using it yet. Why? Two reasons:
- Tons of old devices that can't support it
- Something called **NAT** that's been keeping us alive on IPv4

---

## NAT — the reason we're still surviving on IPv4

NAT lets an entire network share one public IP address. Your whole house — phone, laptop, TV, fridge — goes out to the internet through one IP. That's why we haven't fully switched to IPv6 yet. NAT bought us time.

---

## Why not just use IPv6 from the start?

IPv4 uses decimal — numbers we understand. IPv6 plays in hexadecimal. But honestly that's not the main reason. The real reason is legacy devices. A huge chunk of the world's infrastructure still runs on IPv4 and can't just switch overnight.

---

## IP Classes — yes, like social classes

Networks have classes too. Think of it like society:

| Class | Who it's for |
|-------|--------------|
| A | Governments and massive organizations |
| B | Mid-size companies |
| C | The rest of us |

---

## Public vs Private IP

**Public IP** — visible on the internet, assigned by your ISP (like We or Vodafone).

**Private IP** — only visible inside your own network. You can find it by running:

```bash
ip a        # Linux
ipconfig    # Windows
```

---
 
*Written in my own words — not copy-pasted.*
