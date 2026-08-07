# CricVault – Box Cricket Scoring App

**Hit Hard. Stay In.**

Lightweight offline box-cricket scorer (HTML/CSS/JS). Mobile + desktop.

## Login & permissions

| Username | Password   | Role   | Can do |
|----------|------------|--------|--------|
| `admin`  | `admin123` | Scorer | Full access – score, setup, players |
| `scorer` | `scorer123`| Scorer | Full access – score, setup, players |
| `hari`   | `hari123`  | Scorer | Full access |
| `viewer` | `view123`  | Viewer | Live, scorecard, history only |
| `guest`  | `guest123` | Viewer | Live, scorecard, history only |

- **Scorers** can mark every ball, start matches, add players.
- **Viewers** only watch (keypad locked). Logout from the header.

> **Security note:** This is client-side protection for shared phones / TV display.  
> Usernames and passwords are in the page source. For stronger security, host behind a real backend or password-protect the server.

To add/change users, edit the `USERS` array in `index.html`.

## Team selection

| Mode | Behaviour |
|------|-----------|
| **Common player OFF** | Equal team sizes; other team’s players are hidden |
| **Common player ON** | Pick 1 common player first; then masking returns |

Common player may **bat or bowl**, not both in the same match.

## Key rules

- Chase stops when target is reached  
- After wicket: pick next batsman + who faces  
- Wides / no-balls are not legal balls  
- SR = (runs/balls)×100 · Econ = runs/overs  

## Host on GitHub Pages

1. Public repo → upload `index.html` + `README.md`  
2. Settings → Pages → `main` / root  
3. Open `https://YOUR_USERNAME.github.io/REPO_NAME/`  

## Local host

```bash
python3 -m http.server 9000 --bind 0.0.0.0
```

---

Built for box cricket. 🏏
