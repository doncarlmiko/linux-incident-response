# Linux Incident Response Simulation

This project demonstrates my ability to investigate, triage, and resolve a simulated Linux system incident.  
It’s part of my public DevOps portfolio to show skills in **system administration, process monitoring, debugging, and documentation**.

---

## 🛠️ Project Overview

- **Environment:** [Play With Docker](https://labs.play-with-docker.com/) (Alpine Linux)
- **Incident simulated:** A runaway process created using `yes > /dev/null &`
- **Goal:** Detect the process, investigate its PID, kill it, and verify resolution
- **Deliverables:** Documentation + screenshots of the workflow

---

## 📂 Repository Structure

linux-incident-response/
├── README.md # Repo overview (this file)
├── screenshots/
│ ├── before.png # Process running
│ ├── after.png # Process terminated

## 🚀 How to Reproduce the Incident

### Step 1. Start a runaway process

```bash
yes > /dev/null &
```

### Step 2. Show running processes

```bash
ps
```

👉 Look for a line with yes. Note the PID (process ID number).
📸 Screenshot #1: capture the ps output showing yes running.

### Step 3. Kill the runaway process

```bash
kill -9 <PID>
```

Replace <PID> with the number you found in Step 2. Example:

```bash
kill -9 360
```

### Step 4. Confirm it’s gone

```bash
ps
```

👉 The yes process should no longer appear.
📸 Screenshot #3: capture the ps output after the kill command.
