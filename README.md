# deepseek
DeepSeek R1本地部署全攻略,deepseek从入门手册到精通最全指令汇总,各版本安装包合集！
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DeepSeek R1 完全指南</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        :root {
            --deepseek-blue: #1a73e8;
            --deepseek-gradient: linear-gradient(135deg, #1a73e8 0%, #0d47a1 100%);
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            padding-top: 60px;
        }

        .navbar {
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            background: var(--deepseek-gradient);
        }

        .jumbotron {
            background: var(--deepseek-gradient);
            color: white;
            padding: 4rem 2rem;
            margin-bottom: 2rem;
        }

        .feature-card {
            transition: transform 0.3s;
            border: none;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .feature-card:hover {
            transform: translateY(-5px);
        }

        .code-snippet {
            background: #f8f9fa;
            border-radius: 8px;
            padding: 1rem;
            font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
        }

        .version-badge {
            background-color: var(--deepseek-blue);
        }

        .section-anchor {
            scroll-margin-top: 80px;
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">DeepSeek R1</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#deploy">部署指南</a></li>
                    <li class="nav-item"><a class="nav-link" href="#commands">指令手册</a></li>
                    <li class="nav-item"><a class="nav-link" href="#downloads">安装包</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- 头部横幅 -->
    <header class="jumbotron">
        <div class="container text-center">
            <h1 class="display-4 mb-4">DeepSeek R1 完全指南</h1>
            <img src="assets/header-image.png" alt="DeepSeek R1 架构图" class="img-fluid rounded-3" style="max-height: 400px;">
        </div>
    </header>

    <!-- 主要内容 -->
    <main class="container">
        <!-- 部署指南 -->
        <section id="deploy" class="section-anchor mb-5">
            <h2 class="mb-4">📦 本地部署全攻略</h2>
            <div class="row g-4">
                <div class="col-md-6">
                    <div class="feature-card card h-100 p-3">
                        <img src="assets/deploy-step1.png" class="card-img-top" alt="环境准备">
                        <div class="card-body">
                            <h5>1. 环境准备</h5>
                            <p>系统要求：</p>
                            <ul>
                                <li>Python ≥ 3.8</li>
                                <li>CUDA 11.6+</li>
                                <li>Docker 20.10+</li>
                            </ul>
                            <div class="code-snippet">
                                <code>conda create -n deepseek python=3.9</code>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="feature-card card h-100 p-3">
                        <img src="assets/deploy-step2.png" class="card-img-top" alt="安装流程">
                        <div class="card-body">
                            <h5>2. 安装流程</h5>
                            <p>使用官方安装脚本：</p>
                            <div class="code-snippet mb-3">
                                <code>curl -sSL https://install.deepseek.com | bash</code>
                            </div>
                            <p>验证安装：</p>
                            <div class="code-snippet">
                                <code>deepseek --version</code>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 指令手册 -->
        <section id="commands" class="section-anchor mb-5">
            <h2 class="mb-4">📚 核心指令手册</h2>
            <div class="table-responsive">
                <table class="table table-hover">
                    <thead class="table-dark">
                        <tr>
                            <th>指令</th>
                            <th>参数</th>
                            <th>说明</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><code>deepseek init</code></td>
                            <td>--model <em>MODEL_NAME</em></td>
                            <td>初始化模型配置</td>
                        </tr>
                        <tr>
                            <td><code>deepseek train</code></td>
                            <td>--config <em>PATH</em></td>
                            <td>启动训练流程</td>
                        </tr>
                        <!-- 更多指令行 -->
                    </tbody>
                </table>
            </div>
        </section>

        <!-- 安装包下载 -->
        <section id="downloads" class="section-anchor mb-5">
            <h2 class="mb-4">📦 版本下载中心</h2>
            <div class="row g-4">
                <div class="col-md-4">
                    <div class="card h-100">
                        <div class="card-body">
                            <h5 class="card-title">稳定版 v1.2.3</h5>
                            <span class="badge version-badge">推荐</span>
                            <ul class="mt-2">
                                <li>发布日期：2024-03-15</li>
                                <li>文件大小：856MB</li>
                                <li>SHA256：a1b2c3...d4e5f6</li>
                            </ul>
                            <a href="#" class="btn btn-primary">下载</a>
                        </div>
                    </div>
                </div>
                <!-- 更多版本卡片 -->
            </div>
        </section>
    </main>

    <!-- 页脚 -->
    <footer class="bg-dark text-light py-4 mt-5">
        <div class="container text-center">
            <p>© 2024 DeepSeek 开发者社区 | 问题反馈：support@deepseek.com</p>
            <div class="social-links">
                <a href="#" class="text-light mx-2">GitHub</a>
                <a href="#" class="text-light mx-2">文档中心</a>
                <a href="#" class="text-light mx-2">开发者论坛</a>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
