当Git认为文件有更改而实际上内容未变时，通常由以下原因导致。以下是逐步排查和解决方法：

---

### **1. 行尾符（CRLF/LF）不一致**
不同操作系统使用不同的换行符：
- **Windows**：`CRLF`（`\r\n`）
- **Linux/macOS**：`LF`（`\n`）

Git可能自动转换行尾符，导致工作区与仓库中的文件行尾不一致。

#### **解决方法**
- **检查Git配置**：
  ```bash
  git config --global core.autocrlf
  ```
  - **Windows**：设为 `true`（提交时转LF，检出时转CRLF）
    ```bash
    git config --global core.autocrlf true
    ```
  - **Linux/macOS**：设为 `input`（提交时转LF，检出不转换）
    ```bash
    git config --global core.autocrlf input
  ```
- **重新规范化文件**：
  ```bash
  git rm --cached .
  git add .
  ```
  或使用：
  ```bash
  git add --renormalize .
  ```

---

### **2. 文件权限变化**
Git默认跟踪文件的可执行权限（`mode`）。若文件权限从`644`变为`755`，Git会标记为更改。

#### **解决方法**
- **忽略权限变化**：
  ```bash
  git config core.fileMode false  # 仅当前仓库
  git config --global core.fileMode false  # 全局生效
  ```
- **重置权限（如需保留权限）**：
  ```bash
  git diff  # 查看权限变化
  chmod 644 filename  # 恢复原权限
  ```

---

### **3. 不可见字符或空格变化**
文本编辑器可能引入空格（如行尾空格）或编码字符（如BOM头）。

#### **解决方法**
- **查看详细差异**：
  ```bash
  git diff --ignore-cr-at-eol  # 忽略行尾CR
  git diff -w  # 忽略所有空格
  ```
- **手动清理文件**：
  使用编辑器检查并删除隐藏字符。

---

### **4. Git索引或缓存问题**
Git的索引可能异常，导致误判文件状态。

#### **解决方法**
- **清除缓存并重新添加**：
  ```bash
  git rm --cached filename
  git add filename
  ```

---

### **5. 文件系统时间戳问题**
某些情况下，文件时间戳变化可能导致Git误判（罕见）。

#### **解决方法**
- **强制更新索引时间戳**：
  ```bash
  git add --no-all .  # 更新索引时间戳
  ```

---

### **6. 检查Git属性（`.gitattributes`）**
若仓库中有`.gitattributes`文件，可能配置了过滤器或行尾符规则。

#### **解决方法**
- 检查`.gitattributes`中是否对特定文件类型设置了处理规则，如：
  ```
  *.txt text=auto
  ```
  调整或删除相关规则。

---

### **总结步骤**
1. **检查行尾符配置** → 使用`git config`调整`core.autocrlf`。
2. **忽略权限跟踪** → `git config core.fileMode false`。
3. **清理缓存** → `git rm --cached` + 重新添加文件。
4. **检查隐藏字符** → 用`git diff -w`或编辑器排查。
5. **检查`.gitattributes`** → 修正可能干扰的规则。

执行后提交更改即可解决虚假修改问题。