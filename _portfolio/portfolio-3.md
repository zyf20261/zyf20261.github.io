---
title: "Python大作业数据可视化"
date: 2026-1-12
collection: portfolio
type: "Machine Learning"

excerpt: >
  <strong>1. 整体人群模型评估结果</strong><br/>
  <img src='/images/整体图.png' width='400'><br/><br/>

  <strong>2. 分性别混淆矩阵结果</strong><br/>
  <img src='/images/混淆矩阵.png' width='600'><br/>
  结论:该模型在预测 “无 5 年死亡” 时表现较好，但在识别 “高死亡风险” 人群上能力有限，且存在明显性别差异：<br/>
       模型对女性死亡风险的漏诊率更低，预测更保守。<br/>
       对男性死亡风险的漏诊率相对更高，可能需要进一步优化以减少假阴性。<br/><br/><br/>

  <strong>3. 分性别 Kaplan-Meier 生存曲线结果</strong><br/>
  <img src='/images/生存曲线.png' width='600'><br/><br/>

  <strong>4. 分性别 ROC 结果</strong><br/>
  <img src='/images/roc.png' width='400'><br/><br/>

  <strong>5. 分性别 SHAP 结果</strong><br/>
  <img src='/images/shap.png' width='600'>

---

"使用Matplotlib和seaborn进行探索性数据分析，并通过混淆矩阵和ROC曲线评估Cox回归模型性能，Kaplan-Meier生存曲线比较不同风险组5年心血管死亡，SHAP进行变量解释"
