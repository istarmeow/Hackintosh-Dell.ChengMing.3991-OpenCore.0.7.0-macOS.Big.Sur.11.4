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
