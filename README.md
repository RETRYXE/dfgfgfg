<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Разработка мультимедийного пособия | Метод погружения</title>
    <style>
        :root {
            --primary: #005baa;
            --secondary: #e4181c;
            --light: #f8f9fa;
            --dark: #212529;
            --accent: #ffc107;
        }
        
        body {
            font-family: 'Roboto', Arial, sans-serif;
            line-height: 1.6;
            color: var(--dark);
            margin: 0;
            padding: 0;
            background-color: var(--light);
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        h1 {
            margin: 0;
            font-size: 2.5rem;
        }
        
        h2 {
            color: var(--primary);
            border-bottom: 2px solid var(--accent);
            padding-bottom: 0.5rem;
            margin-top: 2rem;
        }
        
        .intro {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            margin: 2rem 0;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .feature-card {
            background: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
        }
        
        .feature-card h3 {
            color: var(--secondary);
            margin-top: 0;
        }
        
        .timeline {
            position: relative;
            max-width: 1200px;
            margin: 2rem auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 6px;
            background-color: var(--primary);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            background-color: white;
            border: 4px solid var(--secondary);
            border-radius: 50%;
            top: 15px;
            z-index: 1;
        }
        
        .left {
            left: 0;
        }
        
        .right {
            left: 50%;
        }
        
        .left::after {
            right: -12px;
        }
        
        .right::after {
            left: -12px;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin: 2rem 0;
        }
        
        .tech-item {
            background: var(--primary);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-weight: bold;
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
        }
        
        @media screen and (max-width: 768px) {
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item::after {
                left: 18px;
            }
            
            .left::after, .right::after {
                left: 18px;
            }
            
            .right {
                left: 0%;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Мультимедийное пособие по изучению иностранных языков</h1>
            <p>Метод полного погружения с использованием современных технологий</p>
        </div>
    </header>
    
    <div class="container">
        <section class="intro">
            <h2>О проекте</h2>
            <p>В современном мире знание иностранных языков становится необходимостью. Наш проект предлагает инновационный подход к изучению языков через метод полного погружения с использованием мультимедийных технологий.</p>
            <p>Разрабатываемое пособие будет соответствовать образовательным стандартам РФ и учитывать особенности русскоязычных учащихся, помогая преодолеть языковой барьер в кратчайшие сроки.</p>
        </section>
        
        <section>
            <h2>Ключевые особенности</h2>
            <div class="features">
                <div class="feature-card">
                    <h3>Виртуальная языковая среда</h3>
                    <p>Создание реалистичных ситуаций общения через VR-технологии, позволяющие погрузиться в языковую среду, не выходя из дома.</p>
                </div>
                <div class="feature-card">
                    <h3>Адаптивное обучение</h3>
                    <p>Искусственный интеллект анализирует прогресс и подстраивает программу под индивидуальные особенности каждого ученика.</p>
                </div>
                <div class="feature-card">
                    <h3>Геймификация процесса</h3>
                    <p>Игровые механики делают обучение увлекательным, повышая мотивацию и вовлеченность учащихся.</p>
                </div>
            </div>
        </section>
        
        <section>
            <h2>Этапы разработки</h2>
            <div class="timeline">
                <div class="timeline-item left">
                    <div class="timeline-content">
                        <h3>Исследование и анализ</h3>
                        <p>Изучение существующих методик, анализ потребностей учащихся и преподавателей, разработка концепции.</p>
                    </div>
                </div>
                <div class="timeline-item right">
                    <div class="timeline-content">
                        <h3>Проектирование</h3>
                        <p>Создание структуры курса, разработка сценариев взаимодействия, проектирование пользовательского интерфейса.</p>
                    </div>
                </div>
                <div class="timeline-item left">
                    <div class="timeline-content">
                        <h3>Разработка контента</h3>
                        <p>Создание мультимедийных материалов: аудио, видео, интерактивных упражнений, VR-сцен.</p>
                    </div>
                </div>
                <div class="timeline-item right">
                    <div class="timeline-content">
                        <h3>Тестирование</h3>
                        <p>Пилотное внедрение в образовательных учреждениях, сбор обратной связи, доработка продукта.</p>
                    </div>
                </div>
                <div class="timeline-item left">
                    <div class="timeline-content">
                        <h3>Запуск</h3>
                        <p>Публикация финальной версии, методические рекомендации для преподавателей, масштабирование проекта.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section>
            <h2>Используемые технологии</h2>
            <div class="tech-stack">
                <span class="tech-item">HTML5/CSS3/JavaScript</span>
                <span class="tech-item">React/Vue.js</span>
                <span class="tech-item">Node.js</span>
                <span class="tech-item">WebVR/WebXR</span>
                <span class="tech-item">TensorFlow.js</span>
                <span class="tech-item">MongoDB</span>
                <span class="tech-item">AWS/GCP</span>
            </div>
        </section>
        
        <section>
            <h2>Преимущества нашего подхода</h2>
            <ul>
                <li><strong>Соответствие ФГОС:</strong> Пособие разрабатывается с учетом российских образовательных стандартов.</li>
                <li><strong>Доступность:</strong> Возможность использования как в школах/вузах, так и для самостоятельного обучения.</li>
                <li><strong>Мультиплатформенность:</strong> Доступ с компьютеров, планшетов и смартфонов.</li>
                <li><strong>Персонализация:</strong> Адаптация под уровень и темп обучения каждого ученика.</li>
                <li><strong>Эффективность:</strong> Метод погружения доказал свою эффективность в изучении языков.</li>
            </ul>
        </section>
    </div>
    
    <footer>
        <div class="container">
            <p>© 2024 Разработка мультимедийного пособия по освоению иностранного языка методом погружения</p>
            <p>Студенческий проект | Колледж информационных технологий</p>
            <p>Руководитель: [ФИО преподавателя]</p>
        </div>
    </footer>
</body>
</html>
