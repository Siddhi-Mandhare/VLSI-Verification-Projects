# 🔬 VLSI Verification Projects

> *"Building confidence in silicon — one assertion at a time."*

Hey there! 👋 Welcome to my VLSI & Hardware Verification portfolio.

This repository is a collection of projects I've built while diving deep into the world of **RTL design and functional verification**. Each project reflects real engineering challenges — from verifying complex bus protocols to designing packet routers from scratch — all written in **SystemVerilog and Verilog**, using industry-standard methodologies like **UVM**.

Whether you're a fellow verification engineer, a recruiter, or just someone curious about hardware — I hope you find something interesting here. 🚀

---

## 📂 Projects at a Glance

| # | Project | Tech Stack | Highlights |
|---|---------|------------|------------|
| 01 | [AXI Protocol — UVC Development & Verification](./01-axi-protocol-uvc) | SystemVerilog, UVM, SVA | 5-channel handshaking, burst verification, real-time bus compliance |
| 02 | [Asynchronous FIFO — Design & Verification](./02-async-fifo-verification) | SystemVerilog, SVA, QuestaSim | Dual clock domains, CDC corner cases, ~95%+ functional coverage |
| 03 | [Memory Design Verification](./03-memory-design-verification) | SystemVerilog, UVM, QuestaSim | Back-to-back R/W ops, ~90–95% coverage, full UVM environment |
| 04 | [3-Port Packet Router — RTL Design](./04-3-port-packet-router) | Verilog, EDA Playground | Header-based routing, FIFO buffering, backpressure handling |

---

## 🧠 What I've Been Working With

```
Languages       →  SystemVerilog · Verilog
Methodology     →  UVM (Universal Verification Methodology)
Assertions      →  SVA (SystemVerilog Assertions)
Tools           →  QuestaSim · EDA Playground
Concepts        →  CDC · Functional Coverage · RTL Design · Bus Protocols
```

---

## 📁 Project Details

### 01 — AXI Protocol · UVC Development & Verification
> *Verifying one of the most widely used on-chip bus protocols*

Built a complete **UVM-based UVC (Universal Verification Component)** from scratch for the AXI protocol. The environment is fully modular — designed to validate AXI interface behavior independently of any design.

- ✅ Verified all five AXI channels: AW, W, B, AR, R
- ✅ Tested write data interleaving across FIXED, INCR, and WRAP burst types
- ✅ Integrated SVA to catch timing violations and data integrity issues in real time

📁 [`./01-axi-protocol-uvc`](./01-axi-protocol-uvc)

---

### 02 — Asynchronous FIFO · Design & Verification
> *Where two clocks meet — and things get tricky*

Verified an asynchronous FIFO operating across **two independent clock domains** — one of the trickiest problems in digital design. Used pointer synchronization and SVA to ensure nothing gets lost in the crossing.

- ✅ R/W pointer synchronization across independent clock domains
- ✅ SVA checks for pointer validity and full/empty flag correctness
- ✅ ~95%+ functional coverage including wraparound and CDC edge cases

📁 [`./02-async-fifo-verification`](./02-async-fifo-verification)

---

### 03 — Memory Design Verification
> *Making sure every read gets exactly what was written*

Developed a full **UVM testbench** to verify synchronous memory supporting back-to-back read/write operations. Applied formal assertions to catch subtle bugs that random tests often miss.

- ✅ UVM-based environment with Driver, Monitor, Scoreboard, and Sequencer
- ✅ SVA for address validity, protocol compliance, and data consistency
- ✅ ~90–95% functional coverage across address space and operation scenarios

📁 [`./03-memory-design-verification`](./03-memory-design-verification)

---

### 04 — 3-Port Packet Router · RTL Design
> *Routing packets reliably, even when things get congested*

Designed a **3-port packet router** in Verilog — 1 input, 2 outputs — with smart header-based destination decoding. Built in FIFO buffering and a proper VALID/READY handshake to keep data flowing without loss.

- ✅ Header-based routing with dynamic destination decoding
- ✅ FIFO buffering using circular addressing per output port
- ✅ Backpressure handling to prevent data loss under congestion

📁 [`./04-3-port-packet-router`](./04-3-port-packet-router)

---

## 🛠️ Tools & Setup

Most simulations can be run with **QuestaSim** or **ModelSim**. The router project runs on **EDA Playground** (no local setup needed).

```bash
# General simulation command (QuestaSim)
vlog -sv <top_file>.sv
vsim -c <top_module> -do "run -all"
```

Each project folder has its own `README.md` with specific run instructions.

---

## 🤝 Let's Connect

If you have feedback, want to collaborate, or just want to talk hardware — feel free to reach out!

- 💼 [LinkedIn](#)
- 📧 [Email](#)

---

## 📄 License

This repository is open-source under the [MIT License](./LICENSE).

---

<p align="center">Made with curiosity, caffeine, and a lot of waveform debugging ☕📟</p>
