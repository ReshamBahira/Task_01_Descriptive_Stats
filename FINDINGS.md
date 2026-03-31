## Phase 3: Research Findings and Analysis

This phase builds on the statistical summaries developed in Phase 1 and Phase 2 to better understand patterns in political advertising during the 2024 U.S. election cycle. The goal is not just to describe the data, but to interpret what it suggests about campaign behavior, strategy, and data limitations.

### 1. Concentration of Ad Spending

One of the clearest patterns in the dataset is the concentration of ad spending among a small number of major political actors. A handful of organizations and candidate-affiliated pages account for a disproportionately large share of total ad spend. These include high-profile campaign entities associated with leading candidates such as Kamala Harris, Joe Biden, and Donald J. Trump.

At the same time, the dataset contains a large number of smaller advertisers whose spending is minimal. Many ads fall into the lowest spending buckets, and a significant portion of ads have very low or even zero reported spend. This creates a **highly uneven distribution**, where a small group dominates financially while a long tail of smaller participants contributes marginally.

This pattern suggests that digital political advertising is not evenly distributed. Instead, it is driven by well-funded campaigns that have the resources to scale their outreach significantly, while smaller organizations participate more sporadically or at lower intensity.

---

### 2. Temporal Patterns in Ad Activity

The timing of advertisements shows clear alignment with key political events. Monthly trends indicate that ad volume increases during important moments in the election cycle, such as primary elections, debates, and the lead-up to Election Day.

These spikes suggest that campaigns strategically adjust their advertising efforts based on voter attention and media coverage. Rather than maintaining a constant level of advertising, campaigns appear to **intensify spending during high-impact periods** when engagement is likely to be higher.

This behavior reflects a reactive and event-driven strategy, where advertising is used to amplify messaging during moments of political significance.

---

### 3. Candidate Mentions and Messaging Strategy

The dataset shows that certain candidates are mentioned more frequently than others, particularly those who are central to the election. High-frequency mentions tend to align with candidates who are also associated with higher spending levels, indicating a relationship between visibility and financial investment.

In addition to candidate mentions, the data reveals patterns in messaging types. Advocacy and issue-based messages are more common than purely informational content. Campaigns frequently focus on topics such as the economy, governance, and social issues, suggesting that messaging is designed not only to promote candidates but also to shape voter opinions on key policy areas.

This indicates that political advertising is used as both a promotional and persuasive tool, combining candidate visibility with issue framing.

---

### 4. Geographic Patterns

While geographic information is not fully detailed across all records, the available data suggests that ad targeting may vary based on audience characteristics and inferred regional interests. Some ads appear to focus on broader national messaging, while others may be tailored to specific audiences.

However, due to limitations in the dataset—particularly missing or incomplete audience-related fields—it is difficult to draw strong conclusions about geographic targeting. This highlights a gap in the data and suggests that additional information would be needed for a more detailed spatial analysis.

---

### 5. Distribution Characteristics and Outliers

The dataset exhibits strong skewness in several key variables, particularly spend and impressions. Most ads have relatively low values, while a small number of ads have extremely high values. This results in a **long-tailed distribution**, where averages are influenced heavily by outliers.

This pattern became especially clear during the pure Python implementation, where manual calculations highlighted how extreme values affect statistical measures such as the mean. In contrast, Pandas makes it easier to compute these values but can obscure the impact of outliers if not examined carefully.

Understanding this skew is important because it shows that a small number of high-impact ads may drive a large portion of overall engagement.

---

### 6. Data Quality and Missing Values

Another important observation is the presence of missing or incomplete data. Several columns, including `ad_delivery_stop_time`, `bylines`, and `estimated_audience_size`, contain significant gaps.

This raises questions about data completeness and consistency. Missing values may result from:
- incomplete reporting
- differences in ad lifecycle (e.g., ongoing vs completed ads)
- variations in how data is collected or stored

These gaps can affect analysis and should be considered when interpreting results.

---

### 7. Impact of Range-Based Data

A unique aspect of this dataset is that key numeric variables such as spend and impressions are stored as ranges rather than exact values. This required converting them into usable numbers using lower bounds or midpoints.

This introduces some uncertainty into the analysis. For example, using lower bounds may underestimate actual values, while midpoints provide only an approximation. Despite this, the overall trends remain consistent, but it is important to recognize that these figures are estimates rather than precise measurements.

---

### 8. Key Takeaways

Based on the analysis, several key conclusions can be drawn:

- Political ad spending is **highly concentrated** among a small number of major campaigns.
- Advertising activity is **strategically timed** around major political events.
- Messaging is **issue-driven**, with a focus on shaping voter perception in addition to promoting candidates.
- The data shows **strong skewness**, with a few high-value ads dominating overall metrics.
- **Missing and range-based data** introduce limitations that must be considered when interpreting results.

---

### Conclusion

This analysis provides a deeper understanding of how political campaigns use digital advertising during an election cycle. It highlights not only spending patterns, but also strategic decisions related to timing, messaging, and targeting.

By combining both manual and library-based approaches, it becomes clear that while tools like Pandas make analysis more efficient, the deeper insights often come from understanding how the data is structured and processed. This phase reinforces the importance of both technical skills and analytical thinking in working with real-world datasets.
