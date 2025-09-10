# 🔒 Nmap Notes

A personal learning log by [@caldodemiso](https://github.com/caldodemiso).  
This repo documents my progress as I study **Nmap** for network scanning and security testing.

---

## 📂 Current Notes

- [nmap-basics.md](nmap-basics.md) → Introductory notes covering TCP/IP, IP addressing, ports, ICMP, and scanning fundamentals.

---

## 🚀 Why This Repo

- Keep track of what I’m learning about Nmap
- Build a quick-reference playbook of commands and concepts
- Show real progress in network security skills

---

## 🛠️ Handy Commands

```bash
# Default scan (top 1000 TCP ports)
nmap scanme.nmap.org

# Fast scan (top 100 ports, no DNS, faster timing)
nmap -F -n -T4 scanme.nmap.org
```

---

## ⚖️ Disclaimer

All scans are run against **approved test targets** like `scanme.nmap.org`.  
⚠️ Unauthorized scanning of networks you don’t own or have permission for may be illegal.  
This repo is for **educational purposes only**.
