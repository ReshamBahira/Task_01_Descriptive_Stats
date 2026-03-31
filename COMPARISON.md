## Comparison: Pure Python vs Pandas

### Do the results agree?

Overall, the results from both approaches are pretty similar. The key numbers like mean, median, min, max for spend and impressions all line up closely, and the overall trends (like most ads having very low spend and a few having very high spend) are consistent in both versions.

There are a few small differences though. Some of that comes from rounding, since Pandas handles floating point values a bit differently. Another reason is how standard deviation is calculated — in my pure Python code I used population standard deviation, while Pandas uses sample standard deviation by default. There are also slight differences in how missing values are handled and how data types are interpreted.

So while the exact numbers may differ slightly, the overall insights are the same.

---

### Where did pure Python require more decisions?

The pure Python version definitely required more manual work and decisions.

For example, I had to:
- decide what counts as a missing value (like empty strings, "NA", etc.)
- manually parse the spend, impressions, and audience columns since they were stored as dictionary strings
- write my own functions for mean, median, percentiles, and standard deviation
- use collections.Counter to handle categorical data

With Pandas, most of this was handled automatically. Functions like `describe()`, `value_counts()`, and `isna()` made things much easier and faster.

So in a way, Pandas hides a lot of the complexity that you have to deal with explicitly in pure Python.

---

### What did I learn from the pure Python version?

Working through the pure Python version helped me understand the dataset much better.

One big thing I noticed is that columns like spend and impressions are not actually numeric — they’re stored as ranges. That forced me to think about how to convert them (using lower bounds or midpoints), which affects the results.

I also got a clearer sense of the data distribution. For example, a large portion of ads have very low or zero spend, while a small number of ads have very high spend. That skew becomes more obvious when you compute things manually.

Another thing I noticed was where missing values actually exist in the dataset, like in `ad_delivery_stop_time` and `bylines`. Handling those manually made me more aware of data quality issues.

If I had only used Pandas, I think I would have gotten the results faster, but I wouldn’t have understood the structure of the data as deeply.

---

### Final thoughts

Both approaches give similar results, but they serve different purposes.

The pure Python version helped me understand how everything works step by step, while the Pandas version made the analysis much faster and cleaner.

Using both together gave me a better understanding of both the data and the tools.
