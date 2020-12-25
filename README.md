# Dell.ChengMing.3991-OpenCore.0.6.4-macOS.Big.Sur.11.1
硬软件信息：

|   条目   |                                        内容                                         |
| -------- | ----------------------------------------------------------------------------------- |
| Model     | Dell ChengMing 3991                                                                 |
| CPU      | i5-10500 CPU                                                                        |
| GPU      | Intel(R) UHD Graphics 630                                                           |
| Audio    | ALC256                                                                              |
| Disk     | CL1-3D128-Q11 NVMe SSSTC 128GB                                                      |
| OpenCore | OpenCore 0.6.4 Debug                                                                     |
| Dmg      | Install.macOS.Big.Sur.11.1(20C69).with.OpenCore.0.6.4.and.Clover.r5127.and.WEPE.dmg |

## BIOS配置
- General → Advanced Boot Options：全部取消勾选
- System Configuration → SATA Operation：勾选AHCI
- Secure Boot → Secure Boot Enable：取消勾选
- Intel® Software Guard Extensions™ → Intel® SGX™ Enable：选择Disabled
- Power Management → Block Sleep：一般不勾选，否则不能进入深度睡眠，深度睡眠影响可切换
- Virtualization Support → VT for Direct I/O：取消勾选

## 改DVMT 64M和关闭CFG
- Dell ChengMing 3991
    - DVMT to 64M：`setup_var 0xF5 0x02`
    - Disable CFG lock：`setup_var 0x3E 0x00`

## 正常工作
- 网卡正常
- 显卡UHD630正常，显存正常
- 显示紫屏问题已修复
- USB可用（可以尝试USB端口定制）
- WOL开机有效

## 不正常工作
- 声卡无法读取，定制失败，**无法输出声音**
- 更换显示器**可能**紫屏，需重新生成配置文件覆盖，测试同一型号无影响
- HDMI输出不支持2K，暂**只能使用1080P的显示器**
