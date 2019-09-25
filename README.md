# [第二届阿里巴巴大数据智能云上编程大赛] 初赛第24名
<br/>

## 代码总体说明

#### feature-engineer:
  * jd_no_rule jd_编码等规则提取，着重于历史满意度，投递率
  * base_model_10_fold 十折基础模型
  * mean_encode 采用平均编码对简历核心特征处理；并且对过拟合等做着重处理

#### explore:
  * data_exploration数据eda可视化，便于提取特征与规则

#### model:
  * lightgbm_baseline 模型输出
  * ensemble_2model （jd_no_rule+mean_encode）融合模型输出
  * ensemble_3model （jd_no_rule+mean_encode+base_model_10_fold）融合模型输出

#### 后续优化:
  * 尝试过文本匹配，效果一般；貌似赛题都是针对相似文本的
  * 最好的模型结果为jd_no_rule+base_model_10_fold——0.242
  * 可能最好的结果jd_no_rule+mean_encode（10折合更多的特征，调参）——2.5后续引入
  * xgboost建立更完善的线下验证机制，完善目标函数
  * 深度学习+规则+xgboost+lightgbm融合
  * 更全面的数据探索+特征融合

#### 数据：
数据参考链接:https://pan.baidu.com/s/1mWPVAKATgH_5-nKQ_8xlKg  密码:t65m
