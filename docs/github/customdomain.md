# GitHub Pages custom domain name  
# Github Pages 配置自定义域名

Configuring a custom domain for a GitHub Pages site involves setting up DNS records with your domain provider and configuring the custom domain within your GitHub repository settings.

为 GitHub Pages 站点配置自定义域涉及使用域名提供商设置 DNS 记录以及在 GitHub 存储库设置中配置自定义域。
Steps to configure a custom domain for GitHub Pages:

为 GitHub Pages 配置自定义域的步骤：
Ensure your site is hosted on GitHub Pages:
确保您的网站托管在 GitHub Pages 上：
Your repository must be configured to publish a site via GitHub Pages, typically from a specific branch or through GitHub Actions.
您的存储库必须配置为通过 GitHub Pages 发布站点，通常是从特定分支或通过 GitHub Actions 发布。
Acquire a custom domain:
获取自定义域：
Purchase a domain name from a domain registrar (e.g., Google Domains, Namecheap, GoDaddy).
从域名注册商处购买域名（例如 Google Domains、Namecheap、GoDaddy）。
Configure DNS records with your domain provider:
通过您的域名提供商配置 DNS 记录：
For an apex domain (e.g., example.com): Create A records that point to GitHub Pages' IP addresses. The current recommended IP addresses are:

对于顶级域（例如 example.com ）： 创建指向 GitHub Pages 的 IP 地址的 A 记录。 目前推荐的 IP 地址是：
代码

        185.199.108.153
        185.199.109.153
        185.199.110.153
        185.199.111.153
For a www subdomain (e.g., www.example.com): Create a CNAME record that points www to your default GitHub Pages domain (e.g., your-username.github.io).

对于 www 子域名（例如 www.example.com ）： 创建一个 CNAME 记录，将 www 指向您的默认 GitHub Pages 域（例如， your-username.github.io ）。
Configure the custom domain in your GitHub repository:

在您的 GitHub 存储库中配置自定义域：
Navigate to your site's repository on GitHub.

导航到 GitHub 上您网站的存储库。
Click on the "Settings" tab.

点击“设置”选项卡。
In the sidebar, under "Code and automation," click "Pages."

在侧边栏的“代码和自动化”下，单击“页面”。
Under "Custom domain," enter your custom domain (e.g., www.example.com or example.com), then click "Save." This action creates a CNAME file in the root of your source branch. 

在“自定义域名”下，输入您的自定义域名（例如， www.example.com 或 example.com ），然后点击“保存”。 此操作会在源分支的根目录中创建一个 CNAME 文件。
Verify DNS propagation and enforce HTTPS:

验证 DNS 传播并强制实施 HTTPS：
Allow time for DNS changes to propagate (this can take a few minutes to several hours).

留出一些时间让 DNS 更改传播（这可能需要几分钟到几个小时）。
On the GitHub Pages settings page, monitor the "DNS check" status.

在 GitHub Pages 设置页面，监控“DNS 检查”状态。
Once the DNS check is successful, you can optionally select "Enforce HTTPS" to secure your site with an SSL certificate provided by GitHub.

DNS 检查成功后，您可以选择“强制 HTTPS”以使用 GitHub 提供的 SSL 证书保护您的网站。