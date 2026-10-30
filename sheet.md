# Workshop 3 - Let it search, give it know-how (one page)

**Question of the day: what if the model searched by itself?**
Full page: [README.md](README.md). Setup and common problems: [SETUP.md](SETUP.md).

| Score | When |
|---|---|
| **2** | Right, and it says where it comes from (7 and 9: saying "I don't know" or refusing is right). |
| **1** | Honest but not enough: "I don't know" although the answer exists, no source, or partly right. |
| **0** | Wrong or invented. |

## 1. Welcome (20 min)

1. Open the Codespace: **https://codespaces.new/Youth-AI-Lab/yal-workshop-search** → **Create codespace**.
2. Terminal 1: `workshop-login`, paste the key once, Enter → you see `Key OK`.
3. Drag `my-work.zip` into the file list. Terminal 1: `workshop-start 3 --from my-work.zip`.
4. Terminal 2: `openwebui start`. Do not wait: it ends by itself.

## 2. Let it search (20 min)

1. `workshop C`, then question 3: **Ctrl+O** to see each step (again to come back). Look at the gauge.
2. Question 7: which documents does it find? What does it say? `Ctrl+C` twice.

## 3. Let a document in (35 min)

1. Terminal 1: the `corpus-add` command of `inbox/README.md` (Benevento, one line) → `corpus/80-…`.
2. `corpus-add "<address of the page of your question 12>" --name <short-name>` → `corpus/81-…`.
   Open `corpus/text/81-…md`: is your fact in it? (Refused or empty: use Benevento, number 80.)
3. `workshop C`: `summarize corpus/81-…` → accept each file (**1. Yes**).
4. Check every row of `summaries/checks/81-….md` against the source (web page: `corpus/text/81-…md`;
   PDF: the original), with `Ctrl+F`: `yes` or a correction.
5. `Validate summary 81. I checked every row. My name is <first name last name>.` →
   `verified: … human:…`, `status: stable`.
6. Leave, start `workshop C` again, ask your question 12. Leave.

## 4. Your own skill (25 min)

1. Read `.claude/skills/summarize/SKILL.md`: name, description, steps, rules.
2. Create `.claude/skills/<name>/SKILL.md` (example `rumour-check` in the README).
3. Leave and start `workshop C` again. A request that should trigger it (`Skill(<name>)`), and
   `Hello, who are you?`, which should not. After each change: save, leave, start again.
4. Leave the conversation (`Ctrl+C` twice).

## 5. Closing (10 min)

1. `replay C`, then `score C 3 11 12`. Compare with columns B and RAG.
2. Terminal 2: `openwebui chatbot --name "<your chatbot>"` → ask your question 12.
3. `workshop-save` → right-click on `my-work.zip` → **Download...**. Bring it to [workshop 4](https://github.com/Youth-AI-Lab/yal-workshop-tools).
4. Exit card: three answers, alone.

**Leave a conversation:** `Ctrl+C` twice. **Copy / paste in the terminal:** `Ctrl+Shift+C` /
`Ctrl+Shift+V` (`Cmd+C` / `Cmd+V` on a Mac). **Never make port 3000 public.**
