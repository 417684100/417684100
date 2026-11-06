# BSP89 N 沟道 MOSFET Datasheet 参数卡

- 厂商：Infineon
- 型号：BSP89
- 类型：N 沟道增强型 MOSFET
- 封装：SOT-223
- 资料整理日期：2026-11-06

## 一、已确认参数

| 参数 | 数值 |
|---|---:|
| VDS 最大值 | 240 V |
| VGS 最大值 | ±20 V |
| ID | 350 mA |
| VGS(th) | 0.8～2.0 V |
| RDS(on) 典型值 | 4 Ω |
| RDS(on) 最大值 | 6 Ω |
| Qg 典型值 | 4.3 nC |
| Ciss | 80 pF |
| Ptot | 约 1.5～1.8 W |
| RθJA | 约 88.3～115 K/W |
| TJ | -55 ℃～+150 ℃ |

## 二、待补充的条件

以下参数必须与 Datasheet 中原表保持一致，不能只记录数值。

| 参数 | 需要补充 |
|---|---|
| ID | 环境温度、连续或脉冲条件、焊盘条件 |
| VGS(th) | 测试 ID，通常还应注明 VDS=VGS |
| RDS(on) | 对应 VGS、ID 和温度 |
| Qg | 对应 VDS、ID 和 VGS 范围 |
| Ciss | 对应 VDS、VGS 和测试频率 |
| Ptot | 对应环境温度和PCB散热条件 |
| RθJA | 对应铜箔面积和测试板条件 |

## 三、导通电阻测试提醒

仿真使用：

```text
VGS = 5 V
VDD = 5 V
RD = 1 kΩ
```

如果 Datasheet 中 `RDS(on)=4/6 Ω` 是在 VGS=10 V 下测得，则不能直接用6 Ω评价 VGS=5 V 时的性能。

仿真结果可用于判断该工作点是否能导通，但不能替代完整 Datasheet 曲线。

## 四、待补充参数

当前资料未明确给出：

```text
体二极管是否存在
体二极管正向压降 VSD
最大脉冲漏极电流 IDM
栅极漏电流 IGSS
输出电容 Coss
安全工作区 SOA
功率降额曲线
```

未找到的数值不得自行猜测。
