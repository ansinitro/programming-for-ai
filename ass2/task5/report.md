# Short Report

Matrix Factorization (MF) achieved the best performance among the three approaches.  
The RMSE on the test set was **1.12**, compared to **2.46** for User-based CF and **2.33** for Item-based CF.  
This shows that MF captures the latent relationships between users and courses more effectively than similarity-based methods.  
However, in terms of ranking metrics, MF had lower precision@5 (**0.10**) and recall@5 (**0.22**) compared to ItemCF, which reached **0.27 precision** and **0.61 recall**.  
This indicates that while MF predicts rating values more accurately, ItemCF may be better at capturing popular courses that users are likely to rate highly.

The latent factors extracted by MF also provide explainability:  
- **factor_0** → courses {16, 2, 10}  
- **factor_3** → courses {9, 8, 4}  
- **factor_5** → courses {13, 5, 6}  

These groupings suggest hidden themes in the dataset (e.g., practical vs. theoretical courses).  
The training curve shows a smooth decrease in RMSE across epochs, confirming stable convergence.

The influence of hyperparameters was also evident.  
- A larger number of latent factors (**k**) increases expressiveness but risks overfitting.  
- The learning rate (**lr**) controls convergence speed, where too high leads to divergence and too low slows learning.  
- Regularization (**reg**) is necessary to prevent overfitting by penalizing large factor weights.  

In this task, moderate values of **k** and **reg** with a small **lr** gave the best balance between accuracy and stability.

---

**Conclusion**:  
- **MF is the most accurate in rating prediction (lowest RMSE).**  
- **ItemCF performs better in top-N recommendation metrics (precision and recall).**  
- **Hyperparameters (k, lr, reg) significantly influence both convergence and generalization.**
