---
layout: page
css: ["whisper.css"]
---

<h4>1.1. Error messages and Explanation</h4>
<hr class="docutils" />
<dl class="simple">
<dt><em><b>40802-410 set battery run mode failed</b></em></dt><dd><p>
    复测：否<br>
    说明：设置电池run模式失败.<br>
    分析：使用RPV.RUN程序手动设置电池进入run模式，查看CANoe界面电池信息是否正常.<br>
    返修：BMS系统中出现0c7800和293100的报错，发现电池无法闭合继电器。更换IMD后返线.</p>
</dd>
<dt><em><b>40601-170 Minimal cell voltage is lower than limit</b></em></dt><dd><p>
    复测：否<br>
    说明：电池最小电芯电压低于下限.<br>
    分析：查看1-180序号的电芯电压分布.<br>
    返修：更换第六号模组，返线.</p>
</dd>
<dt><em><b>41500-993 Error in plug1, abort by PLC</b></em></dt><dd><p>
    复测：是，将插头1重新插拔后复测<br>
    说明：做脉冲测试时，给插头1供300A大电流时由于PLC报警导致测试中止.<br>
    分析：维修需要检查电流输出端的硬件问题。查看发现电柜中控制电流输入的四个开关存在问题，更换开关后问题解决.<br>
    返修：无.</p>
</dd>
<dt><em><b>41500-993 Error in plug1, abort by PLC</b></em></dt><dd><p>
    复测：是，将插头1重新插拔后复测<br>
    说明：做脉冲测试时，给插头1供300A大电流时由于PLC报警导致测试中止.<br>
    分析：维修需要检查电流输出端的硬件问题。查看发现电柜中控制电流输入的四个开关存在问题，更换开关后问题解决.<br>
    返修：无.</p>
</dd>
<dt><em><b>41600-3650 Pulse test 10s internal resistance relative deviation is out of tolerance</b></em></dt><dd><p>
    复测：否<br>
    说明：做脉冲测试时，给插头1供300A大电流时由于PLC报警导致测试中止.<br>
    分析：维修需要检查电流输出端的硬件问题。查看发现电柜中控制电流输入的四个开关存在问题，更换开关后问题解决.<br>
    返修：无.</p>
</dd>
<dt><em><b>40092-340,360 42402-340,360 The initial switch counter is lower than limit</b></em></dt><dd><p>
    复测：否<br>
    说明：读取电池初始继电器次数，数值低于下限.<br>
    分析：使用CANoe软件中的 <a href="2024-05-21-charge_counter" style="color: #FF8000;">Contactor remain read</a> 查看发现电柜中控制电流输入的四个开关存在问题，更换开关后问题解决.<br>
    返修：无.</p>
</dd>
<dt><em><b>42301-280 CANoe sec tick failed, check Zenzefi license</b></em></dt><dd><p>
    复测：是<br>
    说明：电池唤醒时启动CANoe内置的计数器模块失败，根据详细信息检查Zenzefi证书.<br>
    分析：检查Elook电脑上的zenzefi在线页面，查看在线角色是否完全.<br>
    返修：无.</p>
</dd>
<dt><em><b>42301-280 CANoe sec tick failed, check Network, CANAutomation</b></em></dt><dd><p>
    复测：判断是物理网络连接还是无线连接问题后，进行复测<br>
    说明：UNIPAS电脑通过固定端口给Elook电脑中的CNAoe软件发送命令来启动计时器模块，两者之间的通讯存在问题.<br>
    分析：使用 <a href="2024-05-20-iperf3" style="color: #FF8000;">iperf3工具</a> 进行网络连接检测，若运行失败，需要检查两台电脑之间的网线连接。若运行成功，但丢包率较高，则为无线连接问题<br>
    返修：无.</p>
</dd>
<dt><em><b>40301-140 Error in fault memory</b></em></dt><dd><p>
    复测：检查BMS内部错误后，复测<br>
    说明：BMS内部存在报错.<br>
    分析：手动上电，使用CANoe软件读取BMS内部故障，检查故障是否可消除，是否存在白名单上<br>
    返修：无.</p>
</dd>
