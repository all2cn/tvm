<!--- Licensed to the Apache Software Foundation (ASF) under one -->
<!--- or more contributor license agreements.  See the NOTICE file -->
<!--- distributed with this work for additional information -->
<!--- regarding copyright ownership.  The ASF licenses this file -->
<!--- to you under the Apache License, Version 2.0 (the -->
<!--- "License"); you may not use this file except in compliance -->
<!--- with the License.  You may obtain a copy of the License at -->

<!---   http://www.apache.org/licenses/LICENSE-2.0 -->

<!--- Unless required by applicable law or agreed to in writing, -->
<!--- software distributed under the License is distributed on an -->
<!--- "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY -->
<!--- KIND, either express or implied.  See the License for the -->
<!--- specific language governing permissions and limitations -->
<!--- under the License. -->

常见问题解答
==========================
这份文档涵盖了常见问题解答。

如何安装？
--------------
请参见 [安装步骤](http://docs.tvm.ai/install/)。

TVM和其他IR/DSL项目的关系
---------------------------------------
There are usually two levels of abstractions of IR in the deep learning systems.
NNVM, TensorFlow's XLA and Intel's ngraph uses computation graph representation.
This representation is high level, and can be helpful to perform generic optimizations
such as memory reuse, layout transformation and automatic differentiation.

TVM adopts a low level representation, that explicitly express the choice of memory
layout, parallelization pattern, locality and hardware primtives etc.
This level of IR is closer to directly target hardwares.
The low level IR adopt ideas from existing image processing languages like Halide, darkroom
and loop transformation tools like loopy and polyhedra based analysis.
We specifically focus of expressing deep learning workloads(e.g. recurrence),
optimization for different hardware backends and embedding with frameworks to provide
end-to-end compilation stack.


TVM和libDNN cuDNN的关系
------------------------------
TVM can incorporate these library as external calls. One goal of TVM is to be able to
generate high performing kernels. We will evolve TVM an incremental manner as
we learn from the technics of manual kernel crafting and add these as primitives in DSL.
See also [TVM Operator Inventory](https://github.com/dmlc/tvm/tree/master/topi) for
recipes of operators in TVM.
