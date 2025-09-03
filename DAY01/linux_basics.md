
## 🔍 Searching for `{error code 500}` in Linux – Interview Story

Imagine I'm in a system administrator or DevOps interview, and the interviewer asks:

> **"How would you search for the string `{error code 500}` in your Linux logs?"**

Instead of just jumping into a command, I like to give a brief story that reflects my experience and thought process.

---

### 🎯 The Scenario

*"A few months ago, I was on-call during a deployment for one of our production applications. Suddenly, alerts started firing — users were getting server errors, and the backend logs were our best bet to diagnose the issue fast."*

---

### 🛠️ The Problem

We suspected a server-side issue, particularly HTTP 500 errors — which usually mean something went wrong on our side. Our logs were extensive, so scanning manually wasn’t an option.

---

### 💡 The Solution – Using `grep`

To locate the issue quickly, I ran a command like this:

```bash
grep -R '{error code 500}' /var/log/
```

* `grep` is used for searching plain-text files for lines that match a pattern.
* `-R` makes it recursive, scanning all files and subdirectories.
* `'/var/log/'` is the default system log directory.

---

### ⏱️ Improving Search Performance

If I knew the exact log file — say `app.log` — I’d do:

```bash
grep '{error code 500}' /var/log/app.log
```

To add context (lines before and after the match), I’d use:

```bash
grep -C 3 '{error code 500}' /var/log/app.log
```

Or just lines **after** the match:

```bash
grep -A 5 '{error code 500}' /var/log/app.log
```

---

### 🔄 Bonus: Live Monitoring with `tail`

To monitor this in real-time for future incidents, I’d use:

```bash
tail -f /var/log/app.log | grep '{error code 500}'
```

This allows me to watch the log live and filter for just the error lines.

---

### ✅ The Outcome

*"Within minutes, we found that a third-party API failure was causing unhandled exceptions. After wrapping that call with error handling and deploying a hotfix, errors stopped, and the system stabilized."*

It was a high-pressure moment, but having the right tools and mindset helped resolve the issue quickly.

---

## 🧠 Key Takeaways

* Use `grep` for quick, flexible log searching.
* Add `-C`, `-A`, or `-B` for context.
* Combine with `tail -f` for real-time monitoring.
* Always validate the path and permissions for log files.


