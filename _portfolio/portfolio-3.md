---
title: "Python大作业数据可视化"
date: 2026-1-12
collection: portfolio
type: "Machine Learning"

excerpt: >
  <strong>1. 整体人群模型评估结果</strong><br/>
  <img src='/images/整体图.png' width='400'><br/><br/><br/>

  <strong>2. 分性别混淆矩阵结果</strong><br/>
  <img src='/images/混淆矩阵.png' width='600'><br/><br/>
  结论：该模型在预测 “无 5 年死亡” 时表现较好，但在识别 “高死亡风险” 人群上能力有限，且存在明显性别差异：<br/>
       模型对女性死亡风险的漏诊率更低，预测更保守。<br/>
       对男性死亡风险的漏诊率相对更高，可能需要进一步优化以减少假阴性。<br/><br/>

  <strong>3. 分性别 Kaplan-Meier 生存曲线结果</strong><br/>
  <img src='/images/生存曲线.png' width='600'><br/><br/>
  结论：模型的风险分层在男女性人群中均有效，能显著区分不同生存结局的个体；同时，高风险男性的生存恶化速度更快，而高风险女性的生存率下降相对平缓，这表明该风险分层的预后价值在性别间存在差异，男性高风险人群的死亡风险更突出。<br/><br/>

  <strong>4. 分性别 ROC 结果</strong><br/>
  <img src='/images/roc.png' width='400'><br/><br/>
  结论：该模型对 5 年心血管死亡率的预测能力在男女群体中均表现出色，但存在显著的性别差异：<br/>
  对女性的预测准确性更高（AUC=0.928），对男性的预测准确性稍低（AUC=0.850）。<br/>
  这种差异提示模型在不同性别群体中的表现不一致，在临床应用中需要考虑性别因素的影响。<br/><br/>

  <strong>5. 分性别 SHAP 结果</strong><br/>
  <img src='/images/shap.png' width='600'><br/><br/>
  结论：模型的风险预测在男女群体中共享部分核心特征（如年龄、血清肌酐），但也存在显著的性别差异：<br/>
  男性的风险更多与肾功能（LBXSCR）、血脂（LBXTR）、饮酒习惯相关。<br/>
  女性的风险更多与肾功能（UACR_CAT）、血压（BPXSAR）相关。<br/>
  这一差异也解释了之前 ROC 曲线中模型在女性群体中表现更优的现象，因为模型捕捉到了女性特有的关键风险特征。

---

"使用Matplotlib和seaborn进行探索性数据分析，并通过混淆矩阵和ROC曲线评估Cox回归模型性能，Kaplan-Meier生存曲线比较不同风险组5年心血管死亡，SHAP进行变量解释"
