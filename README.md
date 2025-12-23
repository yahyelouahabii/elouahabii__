# elouahabii__
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بروفايل GitHub</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary-color: #0d1117;
            --secondary-color: #161b22;
            --accent-color: #238636;
            --text-color: #f0f6fc;
            --border-color: #30363d;
        }

        body {
            background-color: var(--primary-color);
            color: var(--text-color);
            line-height: 1.6;
            direction: rtl;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* البنر */
        .banner {
            background: linear-gradient(to left, #1a1f2c, #0d1117);
            height: 280px;
            position: relative;
            overflow: hidden;
            border-bottom: 1px solid var(--border-color);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
        }

        .banner-content {
            position: relative;
            z-index: 2;
            padding: 40px 0;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .banner-title {
            font-size: 2.8rem;
            margin-bottom: 10px;
            background: linear-gradient(to right, #58a6ff, #238636);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        .banner-subtitle {
            font-size: 1.2rem;
            color: #8b949e;
            max-width: 600px;
        }

        .banner-pattern {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.1;
            background-image: 
                radial-gradient(circle at 25% 25%, #58a6ff 2px, transparent 2px),
                radial-gradient(circle at 75% 75%, #238636 2px, transparent 2px);
            background-size: 60px 60px;
        }

        /* المحتوى الرئيسي */
        .profile-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 30px;
            margin-top: -80px;
            position: relative;
            z-index: 3;
        }

        @media (max-width: 768px) {
            .profile-content {
                grid-template-columns: 1fr;
            }
        }

        /* معلومات الملف الشخصي */
        .profile-card {
            background-color: var(--secondary-color);
            border-radius: 12px;
            border: 1px solid var(--border-color);
            padding: 25px;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
        }

        .profile-header {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            margin-bottom: 25px;
        }

        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid var(--accent-color);
            margin-bottom: 20px;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .avatar:hover {
            transform: scale(1.05);
        }

        .profile-name {
            font-size: 1.8rem;
            margin-bottom: 5px;
        }

        .profile-username {
            color: #58a6ff;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .profile-bio {
            color: #8b949e;
            margin-bottom: 20px;
            text-align: center;
        }

        .profile-stats {
            display: flex;
            justify-content: space-around;
            border-top: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
            padding: 15px 0;
            margin-bottom: 20px;
        }

        .stat {
            text-align: center;
        }

        .stat-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: #58a6ff;
        }

        .stat-label {
            font-size: 0.9rem;
            color: #8b949e;
        }

        .profile-links {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .profile-link {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--text-color);
            text-decoration: none;
            padding: 10px 15px;
            border-radius: 8px;
            background-color: rgba(255, 255, 255, 0.05);
            transition: all 0.2s;
        }

        .profile-link:hover {
            background-color: rgba(88, 166, 255, 0.1);
            transform: translateX(-5px);
        }

        /* المشاريع */
        .projects-section {
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 1.8rem;
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--accent-color);
            display: inline-block;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
        }

        .project-card {
            background-color: var(--secondary-color);
            border-radius: 10px;
            border: 1px solid var(--border-color);
            padding: 20px;
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            border-color: #58a6ff;
        }

        .project-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .project-title {
            font-size: 1.3rem;
            color: #58a6ff;
        }

        .project-lang {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.9rem;
            color: #8b949e;
        }

        .lang-color {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .project-desc {
            color: #8b949e;
            margin-bottom: 20px;
            flex-grow: 1;
        }

        .project-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: auto;
        }

        .project-stars {
            display: flex;
            align-items: center;
            gap: 5px;
            color: #8b949e;
        }

        .project-link {
            color: var(--text-color);
            text-decoration: none;
            padding: 8px 15px;
            background-color: var(--accent-color);
            border-radius: 6px;
            transition: background-color 0.2s;
        }

        .project-link:hover {
            background-color: #2ea043;
        }

        /* المهارات */
        .skills-section {
            margin-bottom: 40px;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .skill-tag {
            background-color: rgba(88, 166, 255, 0.1);
            color: #58a6ff;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(88, 166, 255, 0.3);
        }

        /* الفوتر */
        footer {
            text-align: center;
            padding: 30px 0;
            border-top: 1px solid var(--border-color);
            color: #8b949e;
            margin-top: 40px;
        }

        .footer-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }

        .footer-icon {
            color: #8b949e;
            font-size: 1.5rem;
            transition: color 0.2s;
        }

        .footer-icon:hover {
            color: #58a6ff;
        }
    </style>
</head>
<body>
    <!-- البنر -->
    <header class="banner">
        <div class="banner-pattern"></div>
        <div class="container banner-content">
            <h1 class="banner-title">مطور برمجيات مبدع</h1>
            <p class="banner-subtitle">أحب البرمجة والتطوير. أشارك مشاريعي مفتوحة المصدر على GitHub لتعزيز التعلم الجماعي والمساهمة في المجتمع التقني.</p>
        </div>
    </header>

    <main class="container">
        <div class="profile-content">
            <!-- معلومات الملف الشخصي -->
            <aside class="profile-card">
                <div class="profile-header">
                    <img src="https://avatars.githubusercontent.com/u/583231?v=4" alt="صورة الملف الشخصي" class="avatar">
                    <h2 class="profile-name">أحمد محمد</h2>
                    <p class="profile-username">@ahmedmohamed</p>
                    <p class="profile-bio">مطور ويب ومهندس برمجيات مهتم بالتكنولوجيا مفتوحة المصدر</p>
                </div>

                <div class="profile-stats">
                    <div class="stat">
                        <div class="stat-value">48</div>
                        <div class="stat-label">المشاريع</div>
                    </div>
                    <div class="stat">
                        <div class="stat-value">1.2k</div>
                        <div class="stat-label">المتابعون</div>
                    </div>
                    <div class="stat">
                        <div class="stat-value">327</div>
                        <div class="stat-label">المتابَعون</div>
                    </div>
                </div>

                <div class="profile-links">
                    <a href="#" class="profile-link">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>الرياض، السعودية</span>
                    </a>
                    <a href="#" class="profile-link">
                        <i class="fas fa-link"></i>
                        <span>www.ahmeddev.com</span>
                    </a>
                    <a href="#" class="profile-link">
                        <i class="fab fa-twitter"></i>
                        <span>@ahmed_dev</span>
                    </a>
                    <a href="#" class="profile-link">
                        <i class="fas fa-envelope"></i>
                        <span>ahmed@example.com</span>
                    </a>
                </div>
            </aside>

            <!-- المحتوى الرئيسي -->
            <div class="main-content">
                <!-- المشاريع -->
                <section class="projects-section">
                    <h2 class="section-title">المشاريع المميزة</h2>
                    <div class="projects-grid">
                        <!-- مشروع 1 -->
                        <article class="project-card">
                            <div class="project-header">
                                <h3 class="project-title">نظام إدارة المهام</h3>
                                <div class="project-lang">
                                    <span class="lang-color" style="background-color: #f1e05a;"></span>
                                    <span>JavaScript</span>
                                </div>
                            </div>
                            <p class="project-desc">نظام لإدارة المهام الشخصية والجماعية مع واجهة مستخدم تفاعلية ودعم للتطبيقات المحمولة.</p>
                            <div class="project-footer">
                                <div class="project-stars">
                                    <i class="fas fa-star"></i>
                                    <span>342</span>
                                </div>
                                <a href="#" class="project-link">عرض المشروع</a>
                            </div>
                        </article>

                        <!-- مشروع 2 -->
                        <article class="project-card">
                            <div class="project-header">
                                <h3 class="project-title">منصة تعليمية</h3>
                                <div class="project-lang">
                                    <span class="lang-color" style="background-color: #3572A5;"></span>
                                    <span>Python</span>
                                </div>
                            </div>
                            <p class="project-desc">منصة تعليمية مفتوحة المصدر تقدم دورات في البرمجة والذكاء الاصطناعي.</p>
                            <div class="project-footer">
                                <div class="project-stars">
                                    <i class="fas fa-star"></i>
                                    <span>521</span>
                                </div>
                                <a href="#" class="project-link">عرض المشروع</a>
                            </div>
                        </article>

                        <!-- مشروع 3 -->
                        <article class="project-card">
                            <div class="project-header">
                                <h3 class="project-title">أداة تحليل البيانات</h3>
                                <div class="project-lang">
                                    <span class="lang-color" style="background-color: #e34c26;"></span>
                                    <span>HTML/CSS</span>
                                </div>
                            </div>
                            <p class="project-desc">أداة لتحليل وعرض البيانات مع إمكانية تصدير النتائج بصيغ مختلفة.</p>
                            <div class="project-footer">
                                <div class="project-stars">
                                    <i class="fas fa-star"></i>
                                    <span>187</span>
                                </div>
                                <a href="#" class="project-link">عرض المشروع</a>
                            </div>
                        </article>
                    </div>
                </section>

                <!-- المهارات -->
                <section class="skills-section">
                    <h2 class="section-title">المهارات التقنية</h2>
                    <div class="skills-list">
                        <span class="skill-tag">JavaScript</span>
                        <span class="skill-tag">React</span>
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">Node.js</span>
                        <span class="skill-tag">HTML/CSS</span>
                        <span class="skill-tag">Git</span>
                        <span class="skill-tag">SQL</span>
                        <span class="skill-tag">Docker</span>
                        <span class="skill-tag">Azure</span>
                        <span class="skill-tag">UI/UX Design</span>
                    </div>
                </section>
            </div>
        </div>
    </main>

    <footer>
        <div class="container">
            <div class="footer-icons">
                <a href="#" class="footer-icon"><i class="fab fa-github"></i></a>
                <a href="#" class="footer-icon"><i class="fab fa-linkedin"></i></a>
                <a href="#" class="footer-icon"><i class="fab fa-twitter"></i></a>
                <a href="#" class="footer-icon"><i class="fab fa-codepen"></i></a>
            </div>
            <p>© 2023 أحمد محمد. جميع الحقوق محفوظة.</p>
            <p>مستوحى من تصميم GitHub مع تحسينات تفاعلية</p>
        </div>
    </footer>

    <script>
        // إضافة تفاعلية بسيطة للصفحة
        document.addEventListener('DOMContentLoaded', function() {
            // تأثير عند التمرير على البطاقات
            const projectCards = document.querySelectorAll('.project-card');
            
            projectCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-8px)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0)';
                });
            });

            // تغيير لون البنر عند التمرير
            const banner = document.querySelector('.banner');
            
            window.addEventListener('scroll', function() {
                const scrollPosition = window.scrollY;
                if (scrollPosition > 50) {
                    banner.style.opacity = 0.95;
                } else {
                    banner.style.opacity = 1;
                }
            });

            // تحديث عداد المتابعين بشكل تفاعلي
            const followerCount = document.querySelector('.stat:nth-child(2) .stat-value');
            let followers = 1200;
            
            // محاكاة زيادة العداد (في التطبيق الحقيقي سيتم جلب البيانات من API)
            setInterval(() => {
                followers += Math.floor(Math.random() * 3);
                followerCount.textContent = followers.toLocaleString();
            }, 5000);
        });
    </script>
</body>
</html>
