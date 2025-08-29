解决 GitHub SSH 无效问题

当使用 SSH 连接 GitHub 时，如果出现连接失败或提示 Permission denied (publickey)，通常是由于 SSH 配置不正确或密钥未正确添加导致的。

示例错误

` $ ssh git@github.com
git@github.com: Permission denied (publickey)

1. 检查 SSH 密钥是否生成

确保已生成 SSH 密钥。如果未生成，可以使用以下命令创建：

` ssh-keygen -t ed25519 -C "your_email@example.com"
密钥会默认保存在 ~/.ssh/id_ed25519，也可以自定义名称。

2. 添加公钥到 GitHub

将生成的公钥（如 ~/.ssh/id_ed25519.pub）内容复制并添加到 GitHub 的 SSH and GPG keys 设置中。

3. 测试连接

使用以下命令测试 SSH 是否正常连接：

ssh -T git@github.com
如果返回 Hi <username>! You've successfully authenticated...，说明连接成功。

4. 自定义密钥名称的解决方法

如果密钥名称不是默认的 id_ed25519，需要手动指定密钥路径：

方法一：使用 -i 参数指定私钥

ssh -i ~/.ssh/your_custom_key git@github.com
方法二：配置 ~/.ssh/config

在 ~/.ssh/config 文件中添加以下内容：

Host github.com
User git
IdentityFile ~/.ssh/your_custom_key
保存后即可直接使用 ssh git@github.com 连接。

5. 确保 SSH Agent 正常运行

在某些系统中，可能需要启动 SSH Agent 并添加私钥：

eval "$(ssh-agent -s)"
ssh-add ~/.ssh/your_custom_key
通过以上步骤，可以有效解决 GitHub SSH 无效的问题，确保正常连接和操作。