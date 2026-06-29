# 03 — TCP, UDP & The Three-Way Handshake

---

## Where does it live?

Layer 4 of the OSI Model — the Transport Layer.

---

## What does the Transport Layer actually do?

It takes your data and breaks it into smaller pieces called packets.
Think of it like a book — you tear out every page and send them one by one to your friend.

But wait — what if something goes wrong on the way?
That's why each packet gets a **sequence number** — like putting each page in an envelope labeled "page 1 of 200", "page 2 of 200", and so on.

---

## TCP vs UDP

We have two protocols operating here. And yes — protocol just means a set of rules that every company in the world agrees to follow for their networks.

### TCP — Transmission Control Protocol

Use it when the data matters. All of it.

If you're downloading an important file and one piece gets lost, the whole file breaks. TCP makes sure every single packet arrives, in order, no exceptions.

TCP is used in:
- Web browsing (HTTP/HTTPS)
- File transfers
- Email

### UDP — User Datagram Protocol

Use it when speed matters more than perfection.

UDP doesn't wait for missing packets. It just keeps sending. If there's a little jitter along the way — fine. The goal is to get there fast, not perfectly.

UDP is used in:
- Video calls
- Live streaming
- Online gaming

---

## The Three-Way Handshake (TCP only)

Before TCP sends anything, it does a little introduction ritual.

Imagine you knock on my door:

| Step | Who | What | Name |
|------|-----|------|------|
| 1 | You | Knock on the door | SYN |
| 2 | Me | "Who's there?" | SYN-ACK |
| 3 | You | "It's me, let's go" | ACK |

That's it. That's the Three-Way Handshake.
After those three steps, the connection is established and data starts flowing.

---
 
*Written in my own words — not copy-pasted.*
