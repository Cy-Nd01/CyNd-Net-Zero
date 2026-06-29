# 02 — MAC Addresses

---

## What is a MAC Address?

Think of it like your fingerprint. Can your fingerprint ever match your cousin's? Impossible. Same with MAC addresses — no two devices in the world share the same one.

Every device that connects to a network has a NIC (Network Interface Card), and the manufacturer burns the MAC address into it. You can't change it. You can't fake it. It's yours.

Don't believe me? Go check your laptop right now. Actually — don't. If it breaks, you'll have nothing to work on.

---

## Where does it live?

Layer 2 of the OSI Model — the Data Link Layer.

---

## MAC vs IP — why do we need both?

MAC works inside your local network (LAN). The moment data needs to travel outside — through a router, across the internet — MAC can't help anymore. That's where IP takes over.

Think of it this way:
- **MAC** = your identity inside the building
- **IP** = your full address so people can find you from anywhere

---

## Is MAC really permanent?

Here's where it gets interesting. Your router might show you a different MAC address sometimes — a virtual one — to protect your real one. That's called **MAC filtering**, and you can enable it in your router settings.

Why does this matter? Because if someone gets your real MAC address, it's like stealing your ID card and planting it at a crime scene. They can impersonate your device completely.

---

## Reading a MAC Address

A MAC address has 6 parts. The first 3 identify the manufacturer. So if you take the first 4 characters and look them up, you can find out exactly which company made the device.

---

## LAN vs WAN

- **LAN (Local Area Network)** — your local environment. Your home, your office. This is where MAC operates.
- **WAN (Wide Area Network)** — the bigger network connecting everything together. This is where IP takes over.

---

 
*Written in my own words — not copy-pasted.*
