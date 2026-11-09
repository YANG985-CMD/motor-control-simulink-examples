# 02 · IPMSM 弱磁扩速

MTPA_only 和 Field_weakening 两组工况。母线和电流限制相同，比较弱磁前后的转速、电流和转矩。

[下载直接运行包](https://github.com/YANG985-CMD/motor-control-simulink-examples/releases/download/open-and-run-v2.0.0/02-morimoto-1990-field-weakening-open-and-run.zip) · [查看运行验证](verification/open-and-run.json)

## 打开与运行

1. 下载并解压运行包，或者下载本仓库后进入本例的 `model` 文件夹。
2. 将 MATLAB 当前文件夹切换到该目录。
3. 打开 **Morimoto1990_FieldWeakening.slx**，点击「运行」。Scope 显示结果曲线。

双击顶层的 **Experiment_Settings**，在 **Experiment** 下拉框选择工况，再点「运行」。默认选中 `Field_weakening`。

本例采用 **.slx + .sldd**。保留独立参数字典，便于查看电机与控制参数，以及复用离散控制器。

- [Morimoto1990_FieldWeakening.sldd](model/Morimoto1990_FieldWeakening.sldd)
- [Morimoto1990_FieldWeakening.slx](model/Morimoto1990_FieldWeakening.slx)

控制器、采样、逆变器和电机保留在主模型的分层子系统中，可以逐层双击查看原生模块。默认工况已经随模型保存。

![模型总览](images/open-and-run-overview.png)

## 运行验证

使用 MATLAB R2024b 和 Simulink，在干净会话中只复制上述模型文件，直接运行了 2 组工况。与原工程对应轨迹逐点核对，最大绝对差见 [open-and-run.json](verification/open-and-run.json)。图表读数来自本工程仿真。

## 论文依据

S. Morimoto; Y. Takeda; T. Hirasa; K. Taniguchi (1990). *Expansion of Operating Limits for Permanent Magnet Motor by Current Vector Control Considering Inverter Capacity*.

[论文 DOI](https://doi.org/10.1109/28.60058)

## 配套记录

本目录保留已有的原始指标与验证记录。本次重新打包的运行验证单独记录在 `verification/open-and-run.json`，历史发布可从仓库 Releases 查看。
