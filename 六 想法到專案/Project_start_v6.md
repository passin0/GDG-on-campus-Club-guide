# 第 ⑥ 堂｜軟體專案的起點：從想法到真正開始做專案

#### 小前提:雖然這篇文章只會簡單帶過大部分專業的東西，但是建議初學者反覆觀看，尤其開始一個專案或是結束一個專案的時候。

上一堂課，我們講完個人 AI 協作的開發教學，今天從一個問題開始。

「我想做一個 AI Agent／社團 App／記帳工具。」但是我要從哪裡開始，要怎麼做，只要開始寫程式，然後交到某個地方就好了嗎？


> 專案可沒有交作業的按鈕，你要讓你自己、使用者甚至是客戶能使用，還需要做什麼?

那就可以先講一個軟體技術團隊能有什麼工作？

一般人以為的工程師 Belike：
寫程式 > 寫程式 > 寫程式

事實上的工程師需要會：
<details>
<summary>點一下箭頭</summary>

這些
```
Requirements Engineering → Stakeholder Analysis → Problem Definition → Requirements Elicitation → Requirements Specification → Requirements Validation → Scope Definition → Feasibility Analysis → Constraint Identification → Risk Assessment → Project Planning → Work Breakdown Structure → Effort Estimation → Resource Planning → Dependency Management → Scheduling → Architecture Design → System Decomposition → Component Design → Interface Design → Data Modeling → Technology Selection → Design Trade-off Analysis → Implementation Planning → Version Control → Branch Management → 寫程式 → Code Review → Static Analysis → Unit Testing → Integration Testing → System Testing → Acceptance Testing → Test Planning → Test Automation → Continuous Integration → Continuous Delivery → Deployment → Configuration Management → Environment Management → Observability → Logging → Monitoring → Incident Detection → Failure Analysis → Debugging → Root Cause Analysis → Performance Analysis → Security Considerations → Reliability Engineering → Documentation → Knowledge Management → Technical Debt Management → Refactoring → Maintenance → Change Management → Release Management → User Feedback → Requirement Reassessment → Iterative Improvement → 然後不知道為什麼繼續寫程式
```
</details>

所以軟體專案有很難嗎？想知道的話，我們就來開始吧!

## 今天要完成什麼？

以自己的 Idea 為主題，你會做出一份「專案起步包」：
等待備註

---

## 0. 什麼是專案？｜7 分鐘
>「專案（Project）是在獨特背景下，為了創造價值而發起的暫時性措施。」---PMBOK® Guide

看起來很神祕，我引用這句也是覺得這樣很深奧，但是就是三件事：
- 我要完成什麼
- 什麼時候要完成
- 我有多少資源可以用 

所以專案管理，簡單來說就是想辦法在這些限制下，把目標完成。假設你想認識專案管理，那先知道一下這些的差別。
- Project：為了完成一個目標而進行的暫時性工作。
- Program：把多個相關的 Project 組合起來管理。
- Product：Project 最後產生、並持續提供價值的東西。

### 0.1 軟體專案呢 ?
上次課程我們教學了 AI coding 工作流的
> 需求分析、系統設計、程式編寫、測試與維護

在傳統的軟體專案中大致上也是這樣，有個稱呼--瀑布式模型（Waterfall Model），把整個專案週期訂成一條順序階段，在個人開發就足夠使用了。

### 0.2 除了寫程式，我們還可以多做什麼 ?

在我認識的一些人裡面，剛開始想做專案的人可以分成兩種：
一種是我會(用 AI)寫 code 我想做東西，然後就開始讓 AI 寫程式開始迭代，做了一段時間後就開始模糊不太確定下一步要做什麼 ; 
一種是我想做但是我完全不知道從哪裡開始ㄚㄚㄚ(T_T)。

所以我會建議如果遇到以上問題的人可以先嘗試寫給自己一份專案規畫書，用來搞清楚「自己」究竟想做什麼。

同時，這份企劃也會是你用來跟夥伴、教授、客戶、評審交流的第一份重要資料。

所以一個好的軟體專案企畫，可能需要哪些前提?
<details>
<summary>痛點分析</summary>

> 觀察你想解決的問題是什麼人群需要的，可以透過採訪、問卷、研究的形式，去收集各種資料，確認這個痛點是否需要被解決，而不是自己想像的。

如果你找不到問題，像是在黑客松或是提案競賽的時候。可以觀察你的目標客群（主題），從平常的流程開始。

例如：我在台北坐捷運，我每天要進站、拿出手機或是卡片、刷卡、收起來、排隊、找位置、出站也要一樣的流程。

展開流程你就可以總結出來，最大的痛點可能是進出站要操作很麻煩、或是臺灣人很遺憾地不能飛

> 當然，如果是你要開發解決自己問題的工具，也希望採訪一下自己，把自己的問題歸納成幾句話。 
</details>
<details>
<summary>問題定義 </summary>

> 將開頭觀察到的分散痛點，整理成一句具體且可被解決的「核心問題陳述」。

這句話要明確界定這次開發到底要處理的目標是什麼。接下來的所有規劃與迭代都可以回頭看看我們的核心問題。

>像是我們剛剛總結出，台灣人不能飛的痛點，那我們就要定義一個具體問題，本專案旨在解決台灣人不能飛而需要一個替代的大眾外掛工具才能起飛。
</details>
<details>
<summary>客群(使用者)分析</summary>
接著就要釐清這款產品「到底是要做給誰用的」，然後試著描繪出目標使用者的行為習慣、使用情境以及對技術的熟悉程度。
了解使用者是誰，才能設計出符合他們直覺與習慣的產品。

> 如果是你自己，也可以找朋友一起討論看看，你們如果有這類工具可以解決，你們希望怎麼解決。
</details>
<details>
<summary>使用具體情境</summary>
以故事化的方式描述使用者「在什麼時間、什麼地點、遇到了什麼狀況，進而開啟我們的系統」。
幫助團隊產生畫面感，模擬使用者從接觸產品到完成目標的全流程。
這能讓抽象的功能變得具體，更容易發現介面或流程設計上的缺失。
</details>
<details>
<summary>專案目標與範疇 </summary>
</details>
<details>
<summary>功能需求與非功能需求</summary>
</details>
<details>
<summary>架構設計</summary>
</details>
<details>
<summary>技術選用與理由 </summary>
</details>
<details>
<summary>專案開發管理規劃 </summary>
</details>
<details>
<summary>專案品質管理規劃</summary>
</details>
<details>
<summary>專案風險與限制 </summary>
</details>
<details>
<summary>預期成果or效益</summary>
</details>
<details>
<summary>驗證與測試/MVP 測試</summary>
</details>

<small> note：自己開發的時候不一定需要全部都有，但是可以寫下你覺得最重要的項目。 </small>

### 0.3 現代正規專案開發的小補充
---

## 1. 出發點：從痛點拆出真正的問題

使用者需要的是「完成一件事」，不是得到一串按鈕。

```text
我是社團幹部
→ 建立一場活動
→ 填寫資訊
→ 儲存活動頁
→ 其他人可以查看
```

### 練習 ②：我的核心 User Flow

| 步驟 | 使用者做什麼？ | 系統處理什麼？ | 使用者看見什麼？ |
| --- | --- | --- | --- |
| 1 |  |  |  |
| 2 |  |  |  |
| 3 |  |  |  |
| 4 |  |  |  |

若四步內說不清楚，先挑一條最重要的流程；不要把整個產品塞進今天。

---

## 2. MVP：靠「不做什麼」保護專案｜15 分鐘

MVP 不是簡陋版產品，而是用最少功能驗證最核心的價值。

| 校園活動平台 | 第一版做 | 這次不做 |
| --- | --- | --- |
| 活動 | 建立、查看、搜尋活動 | 推薦、地圖、排行榜 |
| 帳號 | 先用簡單身分區分 | 完整登入與社群好友 |
| 溝通 | 顯示基本資訊 | 聊天室、推播通知 |

### 練習 ③：我的範圍卡

使用者最重要的價值：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

第一版必須有：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

這次明確不做：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

> 需求是「快速找到活動」；搜尋框只是其中一種 Feature。不要把解法誤當成需求。

---

## 3. 從需求走到軟體結構｜15 分鐘

需求會逐漸轉換成軟體中的元件。以「使用者可以建立活動」為例：

```text
介面：輸入活動資料、按下建立
    ↓
規則／服務：檢查資料是否完整
    ↓
資料：儲存活動
    ↓
回饋：顯示建立成功或失敗
```

有些專案會再分成 Frontend、API、Backend、Database；小專案也可能先放在同一個地方。重點不是背架構名稱，而是知道：**每個需求都會落到某些責任區塊。**

| 我的第一項需求 | 介面需要什麼？ | 規則需要什麼？ | 資料需要什麼？ | 回饋是什麼？ |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

---

## 4. 切出第一個可交付功能｜12 分鐘

不是「先做一個按鈕」或「先建資料庫」，而是讓使用者能完成一小件有意義的事。

```text
不夠完整：做建立活動按鈕
可交付切片：幹部能填寫活動名稱與日期，送出後看見一筆活動出現在列表中
```

### 練習 ④：功能切片與驗收

第一個功能切片：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

正常使用時，使用者會看見：＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿＿

| 驗收案例 | 預期結果 |
| --- | --- |
| 正常情況 |  |
| 一個例外情況 |  |
| 不應被弄壞的既有行為 |  |

---

## 5. 把專案變成可以開工的工作｜13 分鐘

Project 不是 Task。Task 必須能被完成、驗證、交付。

```text
❌ 做好活動功能
✅ 建立活動資料欄位，能保存 title、date，並在列表顯示一筆新活動
```

| 任務 | 要先完成什麼？ | 完成的證據 | 風險／暫時不做 |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

專案管理的最小版本不是 Jira 或甘特圖，而是知道：**先做什麼、誰負責決定、什麼叫完成。**

---

## 6. 讓 AI 當規劃夥伴｜20 分鐘

### 6.1 先請 AI 幫你追問與比較

```text
這是我的專案想法：［需求一句話］。
目標使用者：［誰］。
核心流程：［貼上流程］。
MVP 包含：［內容］；本次不做：［內容］。

請不要寫 Code。請：
1. 問我最多 5 個最能縮小範圍的問題；
2. 檢查我是否把需求、功能與解法混在一起；
3. 建議一個第一個可驗收功能切片；
4. 標示你做出的假設。
```

### 6.2 再請 AI 產出開工計畫

```text
第一個功能切片是：［內容］。
驗收條件是：［內容］。

請不要直接產生完整專案。請提出：
1. 最小專案結構與每個區塊的責任；
2. 可逐一完成的任務、先後依賴與完成證據；
3. 這次最容易 Scope Creep 的地方；
4. 第一個我現在就能開始做的 Task。
```

檢查 AI 的答案：它有沒有偷加你說過不做的功能？它的 Task 是否能被驗收？哪一項是假設而不是事實？

## 收尾｜5 分鐘：讓專案真的開始

今天的終點不是做完整 App，而是讓你的專案不再停在腦中。

```text
Idea → Problem → Requirement → User Flow → MVP
→ 第一個功能切片 → 結構與任務 → AI Coding → 開工
```

回去後的第一步：建立一份 README，寫下你的問題、MVP、第一個 Task 與完成證據；再讓 AI 協助完成那一件事。
