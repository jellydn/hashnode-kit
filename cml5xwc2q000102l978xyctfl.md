---
title: "Keep Your Global Dev Tools Fresh"
datePublished: Tue Feb 03 2026 01:48:26 GMT+0000 (Coordinated Universal Time)
cuid: cml5xwc2q000102l978xyctfl
slug: keep-your-global-dev-tools-fresh
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/mY9NpmCwwKE/upload/a7752fb3a08bc0d64b85649be457bbf0.jpeg
tags: development, itman

---

One habit that quietly saves me hours every month: **regularly updating global developer tools**. Here’s my simple routine.

### **Go: Update Installed Binaries**

```bash
go install github.com/Gelio/go-global-update@latest
go-global-update
```

This re-installs Go tools at their latest versions in one go.

Perfect for CLIs you installed months ago and never revisited.

### **Rust: Update Cargo-installed Tools**

```bash
cargo install cargo-update
cargo install-update -a
```

Rust tooling evolves fast. cargo-update makes sure your global Cargo tools keep up, safely and predictably.

### **Node.js: Check & Upgrade Global Packages**

```bash
npm install -g npm-check-updates
ncu -g -u
```

Global npm packages tend to rot silently. This keeps them current without manually tracking versions.

### **Bonus: Keep the Toolchain Manager Updated**

```bash
mise self-update
mise up
uv tool update --all
rustup update
```

If you’re using **mise** to manage runtimes and tools, don’t forget to update *mise itself*.

### **Why This Matters**

* Fewer weird bugs
    
* Better performance
    
* New features for free
    
* Less “it works on my machine” energy
    

I usually run all of this **once every 1–2 weeks**, or when something feels… off.

Small habit. Big payoff.