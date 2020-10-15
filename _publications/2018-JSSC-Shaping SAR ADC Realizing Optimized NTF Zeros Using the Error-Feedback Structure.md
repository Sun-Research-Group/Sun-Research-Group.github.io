---
title: "Shaping SAR ADC Realizing Optimized NTF Zeros Using the Error-Feedback Structure"
collection: publications
permalink: /publication/2009-10-01-paper-title-number-1
excerpt: '利用误差反馈结构整形SAR ADC实现优化NTF零点'
date: 2018-10-15
venue: 'Journal 1'
paperurl: 'https://ieeexplore.ieee.org/document/8492338'
citation: 'S. Li, B. Qiao, M. Gandara, D. Z. Pan and N. Sun, "A 13-ENOB Second-Order Noise-Shaping SAR ADC Realizing Optimized NTF Zeros Using the Error-Feedback Structure," in IEEE Journal of Solid-State Circuits, vol. 53, no. 12, pp. 3484-3496, Dec. 2018, doi: 10.1109/JSSC.2018.2871081.'
---


## 概括

这篇文章讲了这样一个故事：在此前的Noise shaping SAR结构上做了两个改进，实现了三个目标。

**两个改进：**

- 在NTF的传递函数上，首次实现了非常接近单位圆的零点。并且这个零点是可以调节的。
- 在电路结构上，上述零点的改进是通过一个error-feedback通路实现的。之前的NSSAR大部分使用了CIFF结构。例如16、17年Wenjuan Guo发了两篇NSSAR，NTF分别是一阶、二阶。都采用了CIFF的结构，需要多输入的比较器，这有噪声和mismatch问题。本文首先在NSSAR中使用了EF结构。具体使用无源FIR和dynamic amplifier实现。

**三个目标：**

- 【非常好的noise shaping效果】，使用FIR优化了零点。在OSR=8的条件下使用 9bit 结构实现了13 ENOB的ADC。
- 【低功耗】。（1）无源EF通路，把信号反馈到输入端的操作是直接用FIR与CDAC 进行chare sharing实现的，fully passive，功耗极低。（2）不需要preamp，连显式的Dynamic amplifier都省掉了，复用比较器。
- 【PVT robustness】通过后端校正实现的。每隔一段时间校正一次，动态调整D-amp的timer，从而调整增益。

**总结：**

总之，这是第一个优化了NTF的、使用EF结构的二阶NSSAR。证明了在NSSAR中可以用简单的电路实现高效的NTF，也证明了EF结构在NSSAR中的有效性。

[Get the paper from IEEE Xplore](https://ieeexplore.ieee.org/document/8492338)

Recommended citation: S. Li, B. Qiao, M. Gandara, D. Z. Pan and N. Sun, "A 13-ENOB Second-Order Noise-Shaping SAR ADC Realizing Optimized NTF Zeros Using the Error-Feedback Structure," in IEEE Journal of Solid-State Circuits, vol. 53, no. 12, pp. 3484-3496, Dec. 2018, doi: 10.1109/JSSC.2018.2871081.