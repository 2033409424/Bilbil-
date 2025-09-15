<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>马金卓 - 前端开发工程师应聘作品集</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #00A1D6;
            --secondary: #FB7299;
            --accent: #FFB11B;
            --light: #F5F7FA;
            --dark: #1F2D3D;
            --success: #52C41A;
            --text: #314659;
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            --bilibili-pink: #FB7299;
            --bilibili-blue: #00A1D6;
        }
        
        body {
            background-color: #f9f9f9;
            color: var(--text);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--bilibili-blue), var(--bilibili-pink));
            color: white;
            padding: 2rem 0;
            text-align: center;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }
        
        header:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.1)"/></svg>');
            background-size: 100% 100%;
        }
        
        .profile {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
            position: relative;
            z-index: 2;
        }
        
        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid rgba(255, 255, 255, 0.3);
            background: linear-gradient(45deg, var(--bilibili-blue), var(--bilibili-pink));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
            font-weight: bold;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }
        
        h2 {
            font-size: 1.8rem;
            margin: 1.5rem 0;
            color: var(--dark);
            position: relative;
            display: inline-block;
        }
        
        h2:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 50px;
            height: 3px;
            background-color: var(--bilibili-blue);
        }
        
        section {
            padding: 4rem 0;
        }
        
        .section-light {
            background-color: white;
        }
        
        .section-dark {
            background-color: var(--light);
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .skill-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
            text-align: center;
        }
        
        .skill-card:hover {
            transform: translateY(-5px);
        }
        
        .skill-card i {
            font-size: 2.5rem;
            color: var(--bilibili-blue);
            margin-bottom: 1rem;
        }
        
        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-img {
            height: 200px;
            background: linear-gradient(45deg, var(--bilibili-blue), var(--bilibili-pink));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        .project-content {
            padding: 1.5rem;
        }
        
        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 1rem 0;
        }
        
        .tag {
            background: var(--light);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background: var(--bilibili-blue);
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: background 0.3s ease;
            border: none;
            cursor: pointer;
            font-weight: 600;
            margin-right: 10px;
            margin-top: 10px;
        }
        
        .btn:hover {
            background: var(--bilibili-pink);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--bilibili-blue);
            color: var(--bilibili-blue);
        }
        
        .btn-outline:hover {
            background: var(--bilibili-blue);
            color: white;
        }
        
        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .contact-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
            text-align: center;
        }
        
        .contact-card i {
            font-size: 2.5rem;
            color: var(--bilibili-blue);
            margin-bottom: 1rem;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }
        
        .about-text {
            line-height: 1.8;
        }
        
        .about-image {
            background: linear-gradient(45deg, var(--bilibili-blue), var(--bilibili-pink));
            height: 300px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem 0;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        
        .social-links a {
            color: white;
            font-size: 1.8rem;
            transition: color 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--bilibili-blue);
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .skills-grid, .projects, .contact-info {
                grid-template-columns: 1fr;
            }
            
            .avatar {
                width: 120px;
                height: 120px;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
        }
        
        /* 动画效果 */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .animate {
            animation: fadeIn 1s ease forwards;
        }
        
        .delay-1 {
            animation-delay: 0.2s;
        }
        
        .delay-2 {
            animation-delay: 0.4s;
        }
        
        .delay-3 {
            animation-delay: 0.6s;
        }
        
        .bilibili-theme {
            color: var(--bilibili-blue);
            font-weight: bold;
        }
        
        .progress-bar {
            height: 8px;
            background: #eee;
            border-radius: 4px;
            overflow: hidden;
            margin: 10px 0;
        }
        
        .progress {
            height: 100%;
            background: linear-gradient(90deg, var(--bilibili-blue), var(--bilibili-pink));
            border-radius: 4px;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
        }
        
        .github-section {
            text-align: center;
            padding: 3rem 0;
            background: linear-gradient(135deg, var(--bilibili-blue), var(--bilibili-pink));
            color: white;
        }
        
        .github-btn {
            display: inline-block;
            margin-top: 1.5rem;
            padding: 1rem 2rem;
            background: white;
            color: var(--bilibili-blue);
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: var(--shadow);
        }
        
        .github-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="profile">
                <div class="avatar">MJZ</div>
                <h1>马金卓</h1>
                <p>前端开发爱好者 | 大一新生 | B站忠实用户</p>
            </div>
        </div>
    </header>

    <section class="section-light">
        <div class="container">
            <h2>关于我</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>您好！我是马金卓，18岁，山东人，目前是一名大一学生。虽然我刚刚开始我的编程之旅，但我对前端开发充满热情，并且渴望在B站这样优秀的平台学习和成长。</p>
                    <p>我从小就对科技和互联网充满好奇，高中时期开始接触编程，并迅速被前端开发所吸引。我喜欢将创意转化为可视化的网页，享受代码在浏览器中运行带来的成就感。</p>
                    <p>作为B站的忠实用户，我深深被其独特的社区文化和优秀的产品体验所吸引。希望能有机会加入B站，为更多用户创造优质的前端体验。</p>
                </div>
                <div class="about-image">
                    <div>热爱编程 · 追求卓越</div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-dark">
        <div class="container">
            <h2>技能展示</h2>
            <div class="skills-grid">
                <div class="skill-card animate">
                    <i class="fab fa-html5"></i>
                    <h3>前端技术</h3>
                    <div class="skill-name">
                        <span>HTML/CSS</span>
                        <span>75%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 75%"></div>
                    </div>
                    <div class="skill-name">
                        <span>JavaScript</span>
                        <span>65%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 65%"></div>
                    </div>
                    <div class="skill-name">
                        <span>React</span>
                        <span>50%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 50%"></div>
                    </div>
                </div>
                <div class="skill-card animate delay-1">
                    <i class="fas fa-mobile-alt"></i>
                    <h3>响应式设计</h3>
                    <p>学习使用Flexbox和Grid布局，能够制作适配各种设备的网页。</p>
                    <div class="skill-name">
                        <span>响应式设计</span>
                        <span>70%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 70%"></div>
                    </div>
                </div>
                <div class="skill-card animate delay-2">
                    <i class="fas fa-tools"></i>
                    <h3>开发工具</h3>
                    <p>熟悉VS Code、Git等开发工具，了解前端开发工作流程。</p>
                    <div class="skill-name">
                        <span>Git</span>
                        <span>60%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress" style="width: 60%"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section-light">
        <div class="container">
            <h2>项目展示</h2>
            <div class="projects">
                <div class="project-card animate">
                    <div class="project-img">个人博客网站</div>
                    <div class="project-content">
                        <h3>响应式博客设计</h3>
                        <p>使用HTML、CSS和JavaScript开发的个人博客网站，完全响应式设计，适配各种设备。</p>
                        <div class="project-tags">
                            <span class="tag">HTML5</span>
                            <span class="tag">CSS3</span>
                            <span class="tag">JavaScript</span>
                        </div>
                        <a href="https://github.com/yourusername/blog-website" class="btn" target="_blank">GitHub代码</a>
                        <a href="https://yourusername.github.io/blog-website" class="btn btn-outline" target="_blank">在线预览</a>
                    </div>
                </div>
                <div class="project-card animate delay-1">
                    <div class="project-img">B站风格播放器</div>
                    <div class="project-content">
                        <h3>视频播放器UI</h3>
                        <p>模仿B站风格的视频播放器界面，包含弹幕功能的基本实现。</p>
                        <div class="project-tags">
                            <span class="tag">HTML5</span>
                            <span class="tag">CSS3</span>
                            <span class="tag">JavaScript</span>
                        </div>
                        <a href="https://github.com/yourusername/bilibili-player" class="btn" target="_blank">GitHub代码</a>
                        <a href="https://yourusername.github.io/bilibili-player" class="btn btn-outline" target="_blank">在线预览</a>
                    </div>
                </div>
                <div class="project-card animate delay-2">
                    <div class="project-img">校园生活小程序</div>
                    <div class="project-content">
                        <h3>校园助手UI设计</h3>
                        <p>为大学生校园生活设计的Web应用界面，包含课程表、活动通知等功能模块。</p>
                        <div class="project-tags">
                            <span class="tag">UI设计</span>
                            <span class="tag">原型设计</span>
                            <span class="tag">Figma</span>
                        </div>
                        <a href="https://github.com/yourusername/campus-assistant" class="btn" target="_blank">GitHub代码</a>
                        <a href="https://yourusername.github.io/campus-assistant" class="btn btn-outline" target="_blank">在线预览</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="github-section">
        <div class="container">
            <h2>我的GitHub项目</h2>
            <p>这里展示了我所有的前端项目代码，欢迎查看和指导！</p>
            <a href="https://github.com/yourusername" class="github-btn" target="_blank">
                <i class="fab fa-github"></i> 访问我的GitHub主页
            </a>
        </div>
    </section>

    <section class="section-dark">
        <div class="container">
            <h2>联系我</h2>
            <div class="contact-info">
                <div class="contact-card animate">
                    <i class="fas fa-envelope"></i>
                    <h3>邮箱</h3>
                    <p>2033409424@qq.com</p>
                </div>
                <div class="contact-card animate delay-1">
                    <i class="fas fa-phone"></i>
                    <h3>电话</h3>
                    <p>19553325375</p>
                </div>
                <div class="contact-card animate delay-2">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>地址</h3>
                    <p>山东 · 中国</p>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2023 马金卓 - 前端开发作品集</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-weibo"></i></a>
                <a href="#"><i class="fab fa-qq"></i></a>
                <a href="#"><i class="fab fa-bilibili"></i></a>
            </div>
            <p>感谢B站提供的机会，期待您的回复！</p>
        </div>
    </footer>

    <script>
        // 简单的动画触发
        document.addEventListener('DOMContentLoaded', function() {
            const animatedElements = document.querySelectorAll('.animate');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                    }
                });
            }, {
                threshold: 0.1
            });
            
            animatedElements.forEach(element => {
                element.style.opacity = 0;
                element.style.transition = 'opacity 0.5s ease-out';
                observer.observe(element);
            });
            
            // 添加B站主题色装饰
            const titles = document.querySelectorAll('h2, h3');
            titles.forEach(title => {
                if (title.textContent.includes('B站') || title.textContent.includes('弹幕')) {
                    title.classList.add('bilibili-theme');
                }
            });
        });
    </script>
</body>
</html>
