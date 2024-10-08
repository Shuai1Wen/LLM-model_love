# LLM-model_love

![](https://github.com/Shuai1Wen/LLM-model_love/blob/main/1.webp)

#大模型项目-省港澳金牌理想恋人培训讲师
--
还在苦恼追不到你心爱的他/她，收获不了甜蜜的爱情而苦恼吗？还在因为每次被发好人卡而伤心吗？还在因为遇到对方的爱情测验没有回答上来降低好感而苦恼吗？

教程安利 如果你也想了解大模型，可以去了解一下哦 [大模型实战营](https://github.com/InternLM/Tutorial)
--


介绍
--
当你正在苦恼追不到你心爱的他/她时，这是一个神奇的恋爱辅导军师，教会你如何在现实生活和心仪的他/她聊天，制造有趣的话题模板，进一步的拉近感情距离;

当你苦恼你的爱情为啥还不来时，这个一个神奇的恋爱培训老师，教会你如何针对不同的女生进行不同的聊天，如何制作有趣的话题，快速拉近距离；

当遇到尴尬的爱情提问时给你满意的回答，成功提升对方的好感。

同时他也是一个富有哲理的爱情哲学家，可以为你的爱情指点迷津，可以解决你的爱情困惑；他还是是一个时尚潮流达人，针对你的穿着给出合理的适合你的建议。

模型特点
--
风格模拟：模拟专业的玄学专家，时尚达人和爱情心理学家，幽默风趣而又不乏正式风格的建议会回答；

互动体验：用户可以通过提问和交流的方式与模型进行互动，就像和一个知心朋友一样给你正确合理有帮助的建议/

本模型是基于Xtuner来进行对应的训练和微调的
# 安装一些必要的库
conda install pytorch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 pytorch-cuda=12.1 -c pytorch -c nvidia -y
# 安装其他依赖
pip install transformers==4.39.3
pip install streamlit==1.36.0

2.3 安装 XTuner
虚拟环境创建完成后，就可以安装 XTuner 了。首先，从 Github 上下载源码。

# 创建一个目录，用来存放源代码
mkdir -p /root/InternLM/code

cd /root/InternLM/code

git clone -b v0.1.21  https://github.com/InternLM/XTuner /root/InternLM/code/XTuner
其次，进入源码目录，执行安装。

# 进入到源码目录
cd /root/InternLM/code/XTuner
conda activate xtuner0121

# 执行安装
pip install -e '.[deepspeed]'

对应的模型参数文件位于：LLM-model_love/finetune_configs中的internlm2_chat_8b文件

通过代码：
cd /root/InternLM/XTuner
xtuner train ./internlm2_chat_1_8b_qlora_alpaca_e3_copy.py --deepspeed deepspeed_zero2 即可开始训练

并通过streamlit run xtuner_streamlit_demo.py进行web可视化
（这里需要对应的端口映射）
#对应的结果示例
![](https://github.com/Shuai1Wen/LLM-model_love/blob/main/2.png)
![](https://github.com/Shuai1Wen/LLM-model_love/blob/main/3.png)


