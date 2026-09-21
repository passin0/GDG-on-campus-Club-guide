如果是你這堂 **「AI Coding：我可以讓 AI 幫我做軟體，而且開始看得懂它」**，我會刻意設計成：

> **概念很少，但每個概念都立刻拿去看 Code / 操作 AI。**

不要變成「90 分鐘軟體工程導論」💀

我會切成下面這個骨架：

---

# 🤖 AI Coding：我可以讓 AI 幫我做軟體，而且開始看得懂它

## 0. 前言｜AI 已經會寫 Code 了，那我們還要學什麼？｜5–10 min

### 先打一個問題

> 「如果 AI 可以幫你寫 500 行 Code，你敢直接把它放進自己的專案嗎？」

展示一段 AI 生成、看起來很複雜的 Code。

然後問：

- 你知道它在哪裡嗎？
- 你知道它在做什麼嗎？
- 如果壞掉，你知道要叫 AI 改哪裡嗎？
- AI 改了 A，為什麼 B 也壞了？

### 核心觀念

> **AI 讓「寫 Code」變便宜，但「理解、判斷、驗證 Code」變得更重要。**

---

# 1. 程式到底在幹嘛？｜10 min

只建立**最低限度的閱讀能力**。

### 1.1 Input → Process → Output

```text
輸入
 ↓
處理
 ↓
輸出
```

### 1.2 Function

讓學生看：

```python
def calculate_total(price, quantity):
    return price * quantity
```

只問：

- Function 是什麼？
- Parameter 是什麼？
- Return 是什麼？

不要開始教 Python 語法大全。

### 1.3 「看懂」的第一個技巧

> **先看它吃什麼、吐什麼，再決定要不要看裡面。**

這裡其實就開始埋後面的 Interface 概念。

---

# 2. 為什麼 Code 要拆開？｜15 min

這裡就是你找到的 ExplainThis 文章可以進場的地方。

## 2.1 一坨 Code vs 模組化

先展示：

```text
app.py
 └── 800 行全部混在一起 💀
```

再展示：

```text
app.py
user.py
database.py
email.py
```

問：

> 「如果登入壞掉，你比較想去哪個專案找？」

---

## 2.2 Module：每一塊負責一件事情

建立最基本的概念：

> **Module = 把複雜的事情切成可以分開理解的部分。**

---

## 2.3 Interface vs Implementation

這個我會特別留。

例如：

```python
send_email(to, subject, content)
```

學生只需要知道：

> 我給它什麼 → 它幫我做什麼

至於：

```text
SMTP
authentication
TLS
retry
network
...
```

**不用懂。**

這會是整堂課非常重要的一個轉折：

> **看懂軟體，不代表你要看懂所有 Code。**

---

# 3. 開始讀 AI 寫的 Code｜10–15 min

這裡從「概念課」正式切進 AI Coding。

給學生一個小專案：

```text
todo-app/
├── app.py
├── todo.py
├── database.py
└── README.md
```

第一個任務：

> **不要問 AI「這份 Code 在幹嘛？」**

而是：

> 「請幫我整理這個專案的模組，以及每個模組的責任。」

---

### 小互動

讓學生猜：

> 「你覺得新增 Todo 應該在哪個檔案？」

再讓 AI 解釋。

這裡會讓他們第一次感受到：

**「原來我可以不用讀完 Code，也能找到我要的地方。」**

---

# 4. AI Coding 的真正工作流｜15 min

這個我會把它變成整堂課的**核心章節**。

不是：

```text
想功能
 ↓
叫 AI 寫
 ↓
祈禱 🙏
```

而是：

```text
Understand
 ↓
Locate
 ↓
Plan
 ↓
Ask AI
 ↓
Review
 ↓
Test
 ↓
Debug
```

逐個解釋，但不用全部深入。

---

## 4.1 Understand

「我要做什麼？」

## 4.2 Locate

「這個功能現在在哪？」

## 4.3 Plan

「我要改哪些地方？」

## 4.4 Ask AI

「請 AI 幫我修改。」

## 4.5 Review

「AI 到底改了什麼？」

## 4.6 Test

「真的能跑嗎？」

## 4.7 Debug

「壞了 → 把錯誤交給 AI → 理解它 → 修。」

---

# 5. 實作：讓 AI 幫你擴充一個真的小軟體｜25–30 min

這裡才是主菜。

不要讓大家從空白資料夾開始。

直接給：

> **一個已經能跑的小型 App**

例如 Todo / 記帳 / 活動管理 / 小型表單。

然後給任務：

### Level 1

> 增加一個欄位

### Level 2

> 增加一個功能

### Level 3

> 自己想一個功能，要求 AI 先說明需要修改哪些 Module。

---

### 強制加入一個規則

🚫 **不能直接叫 AI 修改。**

第一步一定要：

> 「先分析這個功能涉及哪些檔案，以及你預計怎麼修改，不要動 Code。」

學生確認之後：

> 「好，照這個計畫修改。」

這個小規則其實超有價值。

因為他們會開始學：

**AI 是實作工具，不是決策者。**

---

# 6. AI Debug 互動｜10 min

這個可以做得很好玩。

故意給一個壞掉的小功能。

學生看到：

```text
Error 💀
```

不要直接修。

先問：

> 「你覺得是哪裡有問題？」

然後：

> 「請 AI 解釋這個錯誤，不要直接修改。」

再：

> 「根據錯誤原因提出修改方式。」

最後才：

> 「修改。」

這裡可以順便教：

### Error message 不是敵人

而是：

> **給人和 AI 的診斷資訊。**

---

# 7. 收尾：你現在到底學會了什麼？｜5 min

最後不要總結成：

> 今天學了 Function、Module、Interface……💀

而是總結成能力：

### Before

> 「AI 幫我寫了一堆 Code，我不敢碰。」

### After

> 「我知道我要找哪個 Module。」

> 「我知道這個 Function 吃什麼、吐什麼。」

> 「我可以讓 AI 先解釋再修改。」

> 「我知道要 Review 和 Test。」

---

# 最後可以塞一個「額外補充區」

這些我**不一定正式教**，但可以視時間插入：

### 🧠 高內聚 / 低耦合

只講一句：

> **一個模組最好有清楚的責任，而且不要跟其他模組黏得死死的。**

不用開始 SOLID 大全。

---

### 🧠 Technical Debt

> AI 今天幫你快速做完，不代表這份 Code 明天不會變成你的債。💀

這可以非常自然地帶到：

> 「為什麼不能什麼都叫 AI 隨便改？」

---

### 🧠 Code Review

可以問：

> 「如果 AI 是你公司的 Junior Developer，你敢不敢直接 Merge 它的 PR？」

這個問題很好用。

---

### 🧠 Hallucination / AI 產生錯誤

最後提醒：

> **AI 可以很有自信地寫出錯的東西。**

所以：

**Generate ≠ Correct**

---

# 整堂課的時間結構我會抓成

| 章節 | 時間 | 核心 |
|---|---:|---|
| 前言：AI 會寫 Code 了 | 5–10m | 為什麼還要學 |
| ① 程式到底在幹嘛 | 10m | Input / Output / Function |
| ② 為什麼要拆 Code | 15m | Module / Interface |
| ③ 開始讀 AI Code | 10–15m | 找功能、看結構 |
| ④ AI Coding Workflow | 15m | Understand → Plan → Review |
| ⑤ 實作 | 25–30m | AI 擴充既有 App |
| ⑥ Debug 互動 | 10m | Error → AI → 修復 |
| 收尾 | 5m | 能力轉變 |

**總共約 90–100 分鐘，可以依現場壓縮。**

---

而我最想保留的一條主線是：

> **Function → Module → Interface → Project → AI Coding**

因為這會讓學生第一次理解：

**「看懂程式」不是把所有語法學完。**

而是逐漸知道：

> **這東西負責什麼 → 它跟誰溝通 → 我要改功能應該去哪裡 → 我怎麼讓 AI 幫我改 → 我怎麼確認它沒搞事。**

這才真的很像你想要的 **「Vibe Coding → AI Coding」**，而不是換皮的 Prompt Engineering 課。

### 第 5 堂

**我有一個既有專案**

```text
Code
 ↓
Function
 ↓
Module
 ↓
Project
 ↓
Understand
 ↓
AI 修改
```
