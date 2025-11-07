### Project Summary

This project explores predicting rare events in Himalayan expeditions — specifically, deaths during climbs. The dataset I used is small (about 1,030 expeditions over 4 years) and highly imbalanced (only 6 deaths), which makes modeling tricky. I tried different machine learning models, but their accuracy is limited because the minority class is so small. Expanding to the full historical dataset (1950–present) would likely improve results.

In addition to modeling, I explored several key questions about the expeditions, including:

* How climbing status (PSTATUS) varies across mountain ranges (HIMAL_FACTOR)? 

*Climbing status (PSTATUS) across mountain ranges: Most Himalayan ranges have a mix of statuses, but the majority of peaks are successfully summited, with variations reflecting range difficulty.*

* Which mountain ranges have the highest average peak height (HEIGHTM)?

*Mountain ranges with highest average peak height: Kangchenjunga/Simhalila has the highest mean (7,237 m) and median (7,328 m) peak heights.*

* How peak heights differ for open versus closed peaks (OPEN)?

*Peak heights for open vs closed peaks: Most peaks between 6,000–6,999 m are open, while higher peaks (>7,000 m) are more often closed.*

* Which climbing routes (ROUTE1–4) have the highest success rates (SUCCESS1–4)?

*Routes with highest success rates: ROUTE1 dominates with 737 successful climbs; ROUTE2 has 34, and ROUTE3–4 have none.*

* The effect of supplemental oxygen (O2USED, O2NONE) on summit success

&Effect of supplemental oxygen on summit success: Expeditions using oxygen have a 96% success rate versus 60% for those without.*

* How often bad weather (TERMREASON = 4) vs. technical difficulty (TERMREASON = 10) causes expedition termination?

*Bad weather causes 8.7% of terminations, while technical difficulty causes only 1.1%.*

* Whether expeditions with no hired personnel (NOHIRED) have higher or lower death rates?

*Expeditions without hired personnel have a 4.0% death rate, nearly identical to 4.1% for those with hired staff.*

### Model Findings

Dataset: ~1,030 expeditions, 6 deaths (extremely imbalanced).

Random Forest: Excellent at predicting no deaths (majority class), catches most actual deaths (67% recall) but generates many false positives (17% precision).

Logistic Regression: Detects most deaths (67% recall) but very low precision (6%); overall accuracy drops due to imbalance.

XGBoost: Similar to Random Forest — good recall for deaths (~67%) but low precision (~9%), overpredicts rare events.

Bottom line: All models handle the majority class well, detect some deaths, but are unreliable at pinpointing which expeditions will have fatalities. Expanding to the full Himalaya dataset (1950–present) would likely improve performance.

### 📚 Further Reading — Dealing with Small Data & Rare‑Event Predictions

The models in this project face challenges due to small sample sizes and rare events, which make accurate prediction difficult. The following resources provide further reading on strategies for handling small datasets, imbalanced classes, and rare-event modeling in machine learning. They offer practical guidance and examples that can help improve model design and evaluation

* *“What to Do with Small Data”* — Medium article by Rants on Machine Learning: [https://medium.com/rants-on-machine-learning/what-to-do-with-small-data-d253254d1a89](https://medium.com/rants-on-machine-learning/what-to-do-with-small-data-d253254d1a89)
* *“Modeling Rare Event Probability — An Advanced Machine Learning Perspective”* — Medium article by Rahul G: [https://medium.com/@rahulg.isme2325/modeling-rare-event-probability-an-advanced-machine-learning-perspective-2280d5b364c7](https://medium.com/@rahulg.isme2325/modeling-rare-event-probability-an-advanced-machine-learning-perspective-2280d5b364c7)
* Weiss, G., Provost, F.: *“Learning when training data are costly”* (AAAI Workshop paper) — [https://storm.cis.fordham.edu/gweiss/papers/aaai00ws.pdf](https://storm.cis.fordham.edu/gweiss/papers/aaai00ws.pdf)
* *“Machine Learning Rare Event Classification”* — Nature article: [https://www.nature.com/articles/s41524-025-01530-8](https://www.nature.com/articles/s41524-025-01530-8)
* GitHub repo — *“Machine‑Learning‑Rare‑Event‑Classification”* by LeihuaYe: [https://github.com/LeihuaYe/Machine-Learning-Rare-Event-Classification](https://github.com/LeihuaYe/Machine-Learning-Rare-Event-Classification)
* YouTube video — Rare‑Event / Imbalanced Data overview: [https://www.youtube.com/watch?v=flhjn6e6wnY&t=1s](https://www.youtube.com/watch?v=flhjn6e6wnY&t=1s)
* YouTube video — Another take: [https://www.youtube.com/watch?v=gYkgnha68DI](https://www.youtube.com/watch?v=gYkgnha68DI)
* YouTube video — Fraud detection / rare event modelling: [https://www.youtube.com/watch?v=6kwEbsCiLg8](https://www.youtube.com/watch?v=6kwEbsCiLg8)
* Blog post — Python fraud detection / rare‑event example: [https://trenton3983.github.io/posts/fraud-detection-python/](https://trenton3983.github.io/posts/fraud-detection-python/)