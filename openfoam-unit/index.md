# OpenFOAM unit


# OpenFOAM unit
The international system of units (SI) is as follows.

| No.  | Property           | SI unit       | USCS unit                                                    |
| ---- | ------------------ | ------------- | ------------------------------------------------------------ |
| 1    | Mass               | kilogram (kg) | pound-mass (lbm)                                             |
| 2    | Length             | metre (m)     | foot (ft)                                                    |
| 3    | Time               | second (s)    | second (s)                                                   |
| 4    | Temperature        | Kelvin (K)    | degree Rankine (![∘](https://cdn.cfd.direct/docs/user-guide-v8/img/user288x.png)R) |
| 5    | Quantity           | mole (mol)    | mole (mol)                                                   |
| 6    | Current            | ampere (A)    | ampere (A)                                                   |
| 7    | Luminous intensity | candela (cd)  | candela (cd)                                                 |

The Dimension [kg, m, s, K, mol, A, cd]

| Quantity                                                     | Unit              | Unit in openfoam                                          | Dimension         |
| :----------------------------------------------------------- | ----------------- | --------------------------------------------------------- | ----------------- |
| pressure $P$                                                 | $Pa$              | $kg^1 \cdot m^{-1} \cdot s^{-2}$                          | [1 -1 -2 0 0 0 0] |
| velocity $V$                                                 | $m/s$             | $m^1 \cdot s^{-1}$                                        |                   |
| temperature $T$                                              | $K$               | $K^1$                                                     |                   |
| concentration $C_i$                                          | $kg/m^3$          | $kg^1 \cdot m^{3}$                                        |                   |
| body force $\vec{f}$                                         | $N/m^3$           | $kg^1 \cdot m^{-2} \cdot s^{-2}$                          |                   |
| stress tensor $\tau$                                         | $N/m^2$           | $kg^1 \cdot m^{-1} \cdot s^{-2}$                          |                   |
| thermal conductivity $\lambda$                               | $W/(m \cdot K)$   | $kg^1 \cdot m^{-1} \cdot s^{-3} \cdot K^{-1}$             |                   |
| mass diffusivity $D_i$                                       | $m^2/s$           | $m^2 \cdot s^{-1}$                                        |                   |
| 能量源项 $S_f$                                               | $W/m^3$           | $kg^1 \cdot m^{-1} \cdot s^{-3}$                          |                   |
| density $\rho$                                               | $kg/m^3$          | $kg^1 \cdot m^{3}$                                        |                   |
| specific heat capacity $c_p$ <br> 导热系数 热导率            | $J/(kg \cdot K)$  | $m^2 \cdot s^{-2} \cdot K^{-1}$                           |                   |
| [Coefficient of thermal expansion](https://zh.wikipedia.org/zh-cn/热膨胀系数) $\beta$<br>热膨胀系数 | $1/K$             | $K^{-1}$                                                  |                   |
| gravitational acceleration $\vec{g}$                         | $m/s^2$           | $m^1 \cdot s^{-2}$                                        |                   |
| [gas constant](https://zh.wikipedia.org/zh-cn/氣體常數) $R$  | $J/(mol \cdot K)$ | $kg^1 \cdot m^1 \cdot s^{-2} \cdot K^{-1} \cdot mol^{-1}$ |                   |
| molar mass $M$                                               | $kg/mol$          | $kg^{-1} \cdot mol^{-1}$                                  |                   |
| [Enthalpy of fusion](https://en.wikipedia.org/wiki/Enthalpy_of_fusion) $\Delta h$ <br> (latent) heat of fusion <br> 熔化潜热 熔化热 活化焓 | $J/mol$           | $kg^1 \cdot m^1 \cdot s^{-2} \cdot K^{-1} \cdot mol^{-1}$ |                   |
| 活化能 $E$                                                   | $J/mol$           | $kg^1 \cdot m^1 \cdot s^{-2} \cdot mol^{-1}$              |                   |
| [Entropy of fusion](https://en.wikipedia.org/wiki/Entropy_of_fusion) $\Delta S$ <br> 活化熵 | $J/(K \cdot mol)$ | $kg^1 \cdot m^1 \cdot s^{-2} \cdot K^{-1} \cdot mol^{-1}$ |                   |
|                                                              |                   |                                                           |                   |

```bash
#压力名称，单位，数值式;dimensionSet中的值为量纲的指数，且按照上表中的顺序取值。
dimensionedScalar("p",dimensionSet(1,-1,-2,0,0 ,0, 0),0.0);

#如果需要去掉某个volScalarFiled变量的量纲（如：压力），可以使用命令：
p.dimensions().reset(dimless)
```



**reference**  
https://cfd.direct/openfoam/user-guide/v8-basic-file-format/#x17-1290004.2.6

https://blog.csdn.net/hanbingchegu/article/details/112557319

