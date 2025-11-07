### Project Summary

This project explores predicting rare events in Himalayan expeditions — specifically, deaths during climbs. The dataset I used is small (about 1,030 expeditions over 4 years) and highly imbalanced (only 6 deaths), which makes modeling tricky. I tried different machine learning models, but their accuracy is limited because the minority class is so small. Expanding to the full historical dataset (1950–present) would likely improve results.

In addition to modeling, I explored several key questions about the expeditions, including:

* How climbing status (PSTATUS) varies across mountain ranges (HIMAL_FACTOR)
* Which mountain ranges have the highest average peak height (HEIGHTM)
* How peak heights differ for open versus closed peaks (OPEN)
* Which climbing routes (ROUTE1–4) have the highest success rates (SUCCESS1–4)
* The effect of supplemental oxygen (O2USED, O2NONE) on summit success
* How often bad weather (TERMREASON = 4) vs. technical difficulty (TERMREASON = 10) causes expedition termination
* Whether expeditions with no hired personnel (NOHIRED) have higher or lower death rates

I’ve also included a section of further reading on handling small data and rare events in ML, which provides practical guidance and examples for improving model design and evaluation.

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