# QIFIAccount
QIFI协议下的Account实现

_QIFIAccount兼容 [QIFI协议标准](https://github.com/QUANTAXIS/QIFI/blob/master/README.md)和[DIFF协议标准](https://github.com/shinnytech/diff)_

```
pip install qifiaccount
```


### 用法:

参见 /usage 文件夹下的ipython notebook

```python

from QIFIAccount import QIFI_Account, ORDER_DIRECTION
acc = QIFI_Account("x1", "x1")
acc.initial()


print(acc.message)


acc.send_order


acc.cancel_order


acc.get_position

```


QIFI_Account的最优实践是 QIFI_Strategy, 因为QIFI_Account已经将账户层完全实现, 并且支持多市场, 所以 QIFI_Strategy可以直接进行 订阅行情/ 重写on_bar/on_tick 的策略逻辑/ 以及进行仓位/风险管理



StockSim Account

仅限QA模拟盘用户使用(需要申请)