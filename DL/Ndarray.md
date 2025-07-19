#### 构造张量
方法：
```python
import torch
torch.zeros(6,dtype=)
torch.arange(6,dtype=torch.int32)
torch.randn(5,6,7,dtype=torch.float32)
torch.tensor([1,2,3,5])
```
维度问题：
维度`dim=x`，最大的中括号内是`dim=0`，最小的中括号内`dim`最大
广播机制：
```python
a=torch.cat((e,f,...),dim=0)
```

```python
tensor[1,2,3,True,4]
```
在 PyTorch 中，如果列表中包含不同类型的元素，PyTorch 会自动将所有元素转换为兼容的类型。
布尔值 `True` 会被转换为整数1，`False`会被转换为整数0。
数据类型通常会被提升为 `int64`。
```python
tensor[1.,2.]
```
python中用单独的`x.`表示浮点数

`.item()` 是 PyTorch 张量（tensor）的方法，用于将**只包含一个元素的张量**转换为对应的 Python 标量（如 float 或 int），可以配合切片使用。
`X.sum`对张量的所有值代数求和

切片`a[1:2,0:,:4,:]`，切片中`:`含义近于省略与不等号

