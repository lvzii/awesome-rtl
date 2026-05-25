给非 EDA 领域人进入该行业的一些资料。

# Benchmark

| Name         | Category                 | Level                          | Author Org | YEAR-Paper                                                                                                                                     | Link                                                                                                                       | Recommend | Notes                                      |
| ------------ | ------------------------ | ------------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------ |
| CVDP         | RTL generation           |                                | NVIDIA     | -                                                                                                                                              | [github](https://github.com/NVlabs/cvdp_benchmark), [huggingface](https://huggingface.co/datasets/nvidia/cvdp-benchmark-dataset) |           | -                                          |
| RTLLM        | RTL generation           | single module                  | HKUST      | [RTLLM](https://arxiv.org/abs/2308.05345)                                                                                                         | [github](https://github.com/hkust-zhiyao/RTLLM)                                                                               |           | -                                          |
| AssertLLM    | RTL Assertion generation | single module                  | HKUST      | [AssertLLM](https://arxiv.org/abs/2402.00386)                                                                                                     | [github](https://github.com/hkust-zhiyao/AssertLLM)                                                                           |           | -                                          |
| RTL-Coder    | RTL generation           |                                | HKUST      | [RTLCoder](https://zhiyaoxie.com/files/TCAD25_RTLCoder.pdf)                                                                                       | [github](https://github.com/hkust-zhiyao/RTL-Coder)                                                                           |           | -                                          |
| RTLBench     | RTL generation           |                                | NUDT       | [RTLBench](https://www.researchgate.net/publication/399211061_RTLBench_A_Multi-Dimensional_Benchmark_Suite_for_Evaluating_LLM-Generated_RTL_Code) | [github](https://github.com/fangzhigang32/RTLBench)                                                                           |           | -                                          |
| RealBench    | RTL generation           |                                | ICT,CAS    | [RealBench](https://arxiv.org/abs/2507.16200)                                                                                                     | [github](https://github.com/IPRC-DIP/RealBench)                                                                               |           | -                                          |
| RTL-OPT      | RTL Code Optimization    |                                | HKUST      | [RTL-OPT](https://arxiv.org/pdf/2601.01765)                                                                                                       | [anonymous github](https://anonymous.4open.science/r/RTL-OPT-20C5/README.md)                                                  |           | -                                          |
| verilog-eval | RTL generation           | single module                  | NVIDIA     | [VerilogEval](https://arxiv.org/abs/2309.07544), [Revisiting VerilogEval](https://arxiv.org/abs/2408.11053)                                          | [NVlabs/verilog-eval](https://github.com/NVlabs/verilog-eval)                                                                 | ⭐        | -                                          |
| RTL-Repo     | RTL complement           |                                | AUC        | [2024.5-RTL-Repo](https://arxiv.org/abs/2405.17378)                                                                                               | [github](https://github.com/AUCOHL/RTL-Repo), [huggingface](https://huggingface.co/datasets/ahmedallam/RTL-Repo)                 |           | -                                          |
| MEIC         | RTL Debug                | single module                  | SEU        | [2025.5-MEIC-[ICCAD]](https://arxiv.org/pdf/2405.06840)                                                                                                   | [SEU-ACAL/reproduce-MEIC-ICCAD-24](https://github.com/SEU-ACAL/reproduce-MEIC-ICCAD-24)                                       |           | -                                          |
| GenBen       | RTL generation           |                                | -          | [2024.9-GenBen-[OpenReview]](https://openreview.net/forum?id=gtVo4xcpFI)                                                                           | [github](https://github.com/ChatDesignVerification/GenBen)                                                                    |           | -                                          |
| UVLLM        | RTL Debug                | singl module                   | SEU        | [2024.10-UVLLM-[DAC]](https://arxiv.org/abs/2411.16238)                                                                                                 | [amyuch/UVLLM](https://github.com/amyuch/UVLLM)                                                                               |           | -                                          |
| ChipBench    | generate;debug;ref model | single module;multi module;cpu | -          | [2026.2-ChipBench](https://arxiv.org/abs/2601.21448?utm_source=chatgpt.com)                                                                       | [github](https://github.com/zhongkaiyu/ChipBench)                                                                             |           | a full flow framework，several data inside |
| AssertSolver | RTL Debug assertion      | single module                  | SEU        | [2025.3-AssertSolver-[DAC]](https://arxiv.org/abs/2503.04057)                                                                                           | [github](https://github.com/lvzii/AssertSolver)                                                                               | ⭐        | -                                          |
|HWE-Bench | debug |  | PKU | [2026.4-HWE_Bench-[]](https://arxiv.org/pdf/2604.14709) | | | |
# Dataset

| Name | Category | Author Org | Paper | Link | Notes |
| ---- | -------- | ---------- | ----- | ---- | ----- |

# Software

> 部分借助gpt整理

| Name                                             | Type           | 语言支持                  | 特点                | 性能       |
| ------------------------------------------------ | -------------- | ------------------------- | ------------------- | ---------- |
| [Verilator](https://github.com/verilator/verilator) | 编译型仿真     | Verilog/SystemVerilog子集 | 转C++高速仿真       | ★★★★★ |
| Icarus Verilog                                   | 解释型仿真     | Verilog                   | 轻量级              | ★★☆☆☆ |
| GHDL                                             | VHDL仿真       | VHDL                      | 与Yosys结合支持综合 | ★★★☆☆ |
| GTKWave                                          | 波形查看       | VCD/FST                   | Debug波形可视化     | ★★★★☆ |
| [Cocotb](https://www.cocotb.org/)                   | Python验证框架 | Verilog/VHDL              | Python驱动仿真      | ★★★★☆ |

| 工具              | 类型       | 功能             | 适用场景       |
| ----------------- | ---------- | ---------------- | -------------- |
| SymbiYosys        | Formal验证 | BMC/SMT          | 小模块形式验证 |
| Yosys-SMTBMC      | SMT求解    | 有界模型检测     | Assertion验证  |
| JasperGold (商业) | 工业Formal | 完整Property验证 | 工业级验证     |
| OneSpin (商业)    | Formal     | RTL属性验证      | 高端芯片验证   |
| XLS (开源) (not an officially supported Google product)    | IR(中间件语言)(dslx语言写硬件代码->可转rtl)     | Accelerated HW Synthesis      | x   |

# Verilator & UVM

为了纯开源仿真工具使用UVM，使用[verilator支持的uvm](https://github.com/chipsalliance/uvm-verilator)

Opensource is future


[UVM](https://www.accellera.org/downloads/standards/uvm)




# Acknowledgement
Great [CHIPS Alliance](https://www.chipsalliance.org/)! [chisel](https://github.com/chipsalliance/chisel)原来也是他们的