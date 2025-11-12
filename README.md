# 🎬 Sentiment and Text Analysis of *Red One* (2024)  
**Text & Social Media Analytics (Individual Project)**  
**Temasek Polytechnic – School of Informatics & IT**  
**Author:** Adam Haizad Bin Mohamad Faizal (2302276G)  
 

---

## 📘 Project Overview
This project analyzes **audience sentiment and online engagement** surrounding the Christmas action movie *Red One* using **Reddit comments**.  
The aim is to understand how viewers perceive the movie—whether their responses are positive, neutral, or negative—and what key topics drive discussion, such as the **storyline, cast, action scenes, CGI**, or **holiday themes**.

Through **text mining and sentiment analysis** using **SAS Enterprise Miner**, the project uncovers how public opinion aligns with engagement metrics like upvotes, and identifies which aspects of the film contributed most to audience reactions.

---

## 🎯 Objectives
- Identify the **overall audience sentiment** (positive, neutral, or negative) toward *Red One*.  
- Discover **frequently discussed topics** (e.g., actors, storyline, themes).  
- Explore **relationships between sentiment and engagement** (upvotes).  
- Provide **data-driven recommendations** for improving future film releases.  

---

## 🧩 Methodology

### 1️⃣ Data Import
- Created a project named **`TSAL_Indiv_Assignment`** in SAS Enterprise Miner.  
- Imported Reddit comment data into a **File Import Node** for preprocessing.

---

### 2️⃣ Text Parsing Node
- Conducted initial text parsing to extract raw terms and tokens.  
- Added common, uninformative terms such as *movie* and *film* to the **stop word list** to improve relevance.  
- Expanded the stop words list to include frequently used but contextually meaningless terms like *people*, *day*, *yeah*, *time*, *find*, and *Christmas movie*.  
- **Threshold filtering (30 occurrences)** was applied to remove high-frequency, low-value words (based on ChatGPT recommendation).  
- Combined multi-word entities (e.g., `ChrisEvans`, `DwayneJohnson`, `LucyLiu`, `JKSimmons`) to preserve semantic accuracy.  

---

### 3️⃣ Text Filter Node
- Set **Minimum Frequency = 5** to remove extremely rare terms.  
- Grouped **synonyms** to improve data consistency:
  - “good (Adj)” and “good (Noun)” → *good*  
  - “fun (Adj)” and “fun (Noun)” → *fun*  
  - “Rock” (Prop/Noun) → merged under *Dwayne Johnson*  
- Applied **TF-IDF weighting**; removed terms below **0.3** weight threshold.  
- Constructed a **Concept Link diagram** for *Dwayne Johnson* to analyze associations with co-stars and sentiment keywords.

**Key Concept Link Insights:**
- *Dwayne Johnson* was closely linked with *Chris Evans*, *entertaining*, *performance*, and *fan* — indicating strong co-occurrence and high relevance in discussion threads.

---

### 4️⃣ Text Cluster Node
- Used **Text Clustering** to identify major discussion themes.  
- Adjusted number of clusters from **40 → 8 → 4** for optimal distinctiveness.  
- Final four clusters revealed **unique, non-overlapping topics**:
  1. **Christmas Themes** (Santa, Krampus, North Pole)  
  2. **Cast Discussions** (Dwayne Johnson, Chris Evans)  
  3. **Movie Quality & Sentiment** (Good, Bad, Fun)  
  4. **General Entertainment Value**

> Reducing clusters improved clarity and removed repetitive or empty groupings.

---

### 5️⃣ Text Topic Node
- Generated 25 topics initially; reduced to **4 core topics** for interpretability.  
- Aligned each topic with the corresponding cluster for cross-validation.  
- Renamed topics for clarity:

| Topic No. | Topic Name | Core Keywords |
|------------|-------------|----------------|
| 1 | Fun & Enjoyable Christmas Movie | fun, watch, enjoy, amazing |
| 2 | Christmas & Holiday Themes | santa claus, krampus |
| 3 | Cast & Character Discussions | Dwayne Johnson, Chris Evans |
| 4 | Movie Quality & Audience Opinions | good, bad, good movie |

Both **Text Cluster** and **Text Topic** approaches captured similar insights — reinforcing the film’s appeal through entertainment value, star power, and holiday charm.

---

## 📊 Results & Findings

### 🔹 Sentiment Distribution
| Sentiment | Percentage | Interpretation |
|------------|-------------|----------------|
| **Positive** | 56.56% | Majority praise; viewers found it enjoyable and festive. |
| **Neutral** | 21.30% | Balanced or indifferent reactions. |
| **Negative** | 22.14% | Criticisms about plot, CGI, or originality. |

> With over half of all comments positive, *Red One* was **generally well-received**.

---

### 🔹 Engagement vs Sentiment
| Sentiment | Total Upvotes | Avg. Upvotes per Comment |
|------------|----------------|---------------------------|
| Positive | 22,477 | 41.7 |
| Negative | 6,973 | 33.0 |
| Neutral | 3,188 | 15.7 |

💡 **Insight:**  
Even though positive comments were most common, **negative comments attracted significant engagement**, showing that criticism can drive discussion.

---

## 🧠 Discussion
- Frequent mentions of **Dwayne Johnson** confirm his central role in the film’s audience attention.  
- Sentiment trends align with expectations:  
  - High positivity driven by **cast chemistry and festive theme**.  
  - Negativity linked to **CGI quality and story depth**.  
- Upvote analysis shows that **critical comments still foster engagement**, reflecting an active audience dialogue rather than simple approval or disapproval.

---

## 💡 Recommendations
1. **Enhance CGI and storyline depth** to reduce negative sentiment.  
2. **Leverage star power** — Chris Evans and Dwayne Johnson draw strong engagement.  
3. **Maintain seasonal releases** — holiday-themed films attract wide audience attention.  
4. **Monitor social feedback** in real-time for iterative improvement in future productions.  

---

## 🧰 Tools & Techniques
- **Software:** SAS Enterprise Miner  
- **Nodes Used:** File Import, Text Parsing, Text Filter, Text Cluster, Text Topic  
- **Analytical Methods:**  
  - Stop word filtering  
  - Synonym grouping  
  - TF-IDF weighting  
  - Concept linking  
  - Cluster and topic modeling  
  - Sentiment–engagement correlation  

---

## 🧾 Key Takeaways
- *Red One* achieved **56.6% positive reception** with strong emphasis on cast and holiday themes.  
- **Negative sentiment (22.1%)** was mainly linked to CGI and plot, yet drove **high comment engagement**.  
- The project validated hypotheses on viewer perception, actor prominence, and engagement trends.  
- SAS text mining proved effective for extracting themes and quantifying sentiment from social media.

---

## 👤 Author
**Adam Haizad Bin Mohamad Faizal**  
🎓 Diploma in Big Data & Analytics (T60)  
Temasek Polytechnic – School of Informatics & IT  

---

## ⚠️ Disclaimer
> This analysis uses **synthetic or publicly available Reddit data** for educational purposes.  
> It was completed as part of **Temasek Polytechnic’s CIA2E01: Text & Social Media Analytics** coursework and contains **no confidential or personal information**.
