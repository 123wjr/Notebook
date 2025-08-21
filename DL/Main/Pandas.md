>[!Note] 小结
>预处理原始数据，并将原始数据转换为张量格式

[用户指南 — pandas 2.3.0 文档 - pandas 数据分析库](https://pandas.ac.cn/docs/user_guide/index.html)

## `IO`操作
[IO 工具 (文本, CSV, HDF5, …) — pandas 2.3.0 文档 - pandas 数据分析库](https://pandas.ac.cn/docs/user_guide/io.html)
```Python 
import panda as pd
data = pd.read_csv(data_file)
```
读取为`read_xxx`，写入通常为`to_xxx`

## 缺失值
`NaN`代表缺失值，`pd.nan`用于填入`NaN`

数据类型：
`Series`：
`Dataframe(df)`：每一列一个`dtype`，·
