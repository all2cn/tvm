重要！由于国内访问github不便，项目已经迁移至https://gitee.com/all2cn/tvm。

# 前言
欢迎大家一起加入，一一对应翻译官方的每篇文章，造福其他国人！

群星术译
2019.9.26

# 项目信息
* 项目名称：TVM
* 官方地址：https://docs.tvm.ai/
* 项目介绍：
TVM is an open deep learning compiler stack for CPUs, GPUs, and specialized accelerators. It aims to close the gap between the productivity-focused deep learning frameworks, and the performance- or efficiency-oriented hardware backends. TVM provides the following main features:

Compilation of deep learning models in Keras, MXNet, PyTorch, Tensorflow, CoreML, DarkNet into minimum deployable modules on diverse hardware backends.
Infrastructure to automatic generate and optimize tensor operators on more backend with better performance.
TVM stack began as a research project at the SAMPL group of Paul G. Allen School of Computer Science & Engineering, University of Washington. The project is now driven by an open source community involving multiple industry and academic institutions. The project adopts Apache-style merit based governace model.

TVM provides two level optimizations show in the following figure. Computational graph optimization to perform tasks such as high-level operator fusion, layout transformation, and memory management. Then a tensor operator optimization and code generation layer that optimizes tensor operators. More details can be found at the techreport.

# 协议
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/deed.zh"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/80x15.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/deed.zh">知识共享署名-相同方式共享 4.0 国际许可协议</a>进行许可。
