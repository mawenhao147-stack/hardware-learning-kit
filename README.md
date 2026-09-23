# 硬件入门学习包：从基础元器件到 ESP32

> 🌍 **在线访问（GitHub Pages）**：https://mawenhao147-stack.github.io/hardware-learning-kit/
> 📦 **仓库地址**：https://github.com/mawenhao147-stack/hardware-learning-kit
> 🌐 **想直接在浏览器里读？** 双击打开 [index.html](index.html) —— 全部 31 篇文档 + 64 张图例的网页版，带侧边目录与搜索，离线可用。
> 🧮 **要算电阻/分压/功耗？** 打开 [工具箱.html](工具箱.html)。

> 一套可以「照着学、照着搭、照着画」的硬件自学资料。
> 特点：**每个知识点都配图例**（`figures/` 目录，SVG 源文件 + PNG 高清图），并附带一个可离线使用的交互式计算工具箱。

## 怎么用这套资料

1. 先看 `00-学习路线图.md`，确认自己从哪个阶段开始。
2. 按章节顺序阅读，**每读一个图例，就在面包板或仿真里复现一次**。
3. 遇到计算（限流电阻、分压、RC 截止频率、功耗续航）打开 `工具箱.html` 直接算。
4. 学完第 4 章后，从 `06-项目实战` 里挑一个项目做出来，做不出来就回 `04-ESP32单片机/08-常见问题排查.md`。

## 目录

| 章节 | 内容 | 你会获得的能力 |
|---|---|---|
| [00-学习路线图](00-学习路线图.md) | 六阶段路线、时间投入、检查点 | 知道自己在哪、下一步做什么 |
| [01-基础元器件](01-基础元器件/01-电阻.md) | 电阻/电容/电感/二极管/三极管/MOS/继电器/晶振… | 看懂符号、读得懂参数、选得对型号 |
| [02-电路基础与定律](02-电路基础与定律/01-电压电流电阻与欧姆定律.md) | 欧姆定律、基尔霍夫、分压分流、RC、电源、ADC/PWM、总线 | 会算、会估、会验证 |
| [03-小型电路图实战](03-小型电路图实战/01-如何读懂一张原理图.md) | 读图方法、10 个必会小电路、KiCad 入门 | 能读图、能搭电路、能画自己的板子 |
| [04-ESP32单片机](04-ESP32单片机/01-认识ESP32家族.md) | 芯片家族、引脚、最小系统、环境搭建、外设代码、模块接线、低功耗、排错 | 独立完成一个联网/传感/控制项目 |
| [05-工具与焊接](05-工具与焊接/01-工具清单与万用表.md) | 万用表、面包板、焊接、调试仪器 | 动手不把板子烧掉 |
| [06-项目实战](06-项目实战/01-十个循序渐进项目.md) | 10 个递进项目 + 采购清单与预算 | 把知识变成作品 |
| [工具箱.html](工具箱.html) | 色环/欧姆/LED限流/分压/RC/功耗续航 交互计算 | 少按计算器、少烧元件 |

## 图例总览（figures/）

| 图 | 说明 |
|---|---|
| ![路线图](figures/roadmap.png) | 学习路线 |
| ![无源符号](figures/symbols-passive.png) | 无源元件与电源符号 |
| ![半导体符号](figures/symbols-semi.png) | 半导体器件符号 |
| ![接口符号](figures/symbols-io.png) | 开关/机电/接口符号 |
| ![色环](figures/resistor-color-code.png) | 电阻色环与贴片丝印 |
| ![电容](figures/cap-types.png) | 电容类型与选型 |
| ![RC](figures/rc-charge-curve.png) | RC 充放电与时间常数 |
| ![二极管](figures/diode-iv.png) | 二极管特性与 LED 限流 |
| ![分压](figures/voltage-divider.png) | 分压电路 |
| ![滤波](figures/rc-filter.png) | RC 滤波与截止频率 |
| ![三极管开关](figures/npn-switch.png) | 三极管开关与续流二极管 |
| ![MOS](figures/mos-switch.png) | MOS 高低边与电平转换 |
| ![H桥](figures/hbridge.png) | H 桥电机驱动 |
| ![555](figures/555-astable.png) | 555 无稳态振荡器 |
| ![引脚图](figures/esp32-devkit-pinout.png) | ESP32 开发板引脚图 |
| ![GPIO表](figures/esp32-gpio-map.png) | GPIO 能力总表 |
| ![启动](figures/esp32-strapping.png) | 启动模式与自动下载 |
| ![最小系统](figures/esp32-min-system.png) | ESP32 最小系统五要素 |
| ![接线](figures/esp32-periph-wiring.png) | 常用模块接线 |
| ![功耗](figures/esp32-sleep-currents.png) | 功耗等级与续航 |
| ![总线](figures/bus-timing.png) | UART/I2C/SPI 时序 |
| ![面包板](figures/breadboard-anatomy.png) | 面包板内部结构 |
| ![万用表](figures/multimeter.png) | 万用表三种测量 |
| ![焊接](figures/soldering.png) | 焊接要点与好焊点 |
| ![无源实物](figures/physical-passive.png) | 无源/机电件实物图鉴 |
| ![半导体实物](figures/physical-semi.png) | 半导体实物与引脚 |
| ![模块实物](figures/physical-modules.png) | 常用模块实物图鉴 |
| ![开发板解剖](figures/esp32-board-anatomy.png) | ESP32 开发板解剖 |

## 约定与安全

- 文中电压/电流如无特别说明，指直流稳态值。
- **ESP32 GPIO 耐压约 3.6V**：任何 5V 信号进 GPIO 前必须分压或电平转换。
- 锂电池、12V 以上电源、市电（220V）属于危险源：市电部分本资料只讲原理不给实操，强电请找专业人士。
- 上电前养成「三查」习惯：查电源极性、查有无短路（通断档）、查信号电平。
