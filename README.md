# <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BalanceNutrition - Personalized Weight Loss Through Balanced Nutrition</title>
    <style>
        :root {
            --primary-color: #4CAF50;
            --secondary-color: #2196F3;
            --accent-color: #FF9800;
            --text-color: #212121;
            --light-text: #757575;
            --background-color: #FFFFFF;
            --light-background: #F5F5F5;
            --protein-color: #8BC34A;
            --carbs-color: #FFC107;
            --fat-color: #FF5722;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', Arial, sans-serif;
        }
        
        body {
            color: var(--text-color);
            background-color: var(--background-color);
            line-height: 1.6;
        }
        
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        .logo span {
            color: var(--accent-color);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--accent-color);
        }
        
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1490645935967-10de6ba17061?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80' );
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            margin-top: 60px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #e68a00;
        }
        
        section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        .section-title p {
            color: var(--light-text);
            max-width: 700px;
            margin: 0 auto;
        }
        
        .about {
            background-color: var(--light-background);
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            padding-right: 2rem;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
        }
        
        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .features {
            background-color: white;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .feature-card {
            background-color: var(--light-background);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        .feature-card h3 {
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .how-it-works {
            background-color: var(--light-background);
        }
        
        .steps {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        
        .step {
            flex: 1;
            min-width: 250px;
            text-align: center;
            padding: 1rem;
        }
        
        .step-number {
            display: inline-block;
            width: 50px;
            height: 50px;
            background-color: var(--primary-color);
            color: white;
            border-radius: 50%;
            line-height: 50px;
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 1rem;
        }
        
        .step h3 {
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .nutrition-formula {
            background-color: white;
        }
        
        .formula-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
        }
        
        .formula-text {
            flex: 1;
            min-width: 300px;
            padding-right: 2rem;
        }
        
        .formula-chart {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .macro-chart {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            background: conic-gradient(
                var(--protein-color) 0% 30%,
                var(--carbs-color) 30% 75%,
                var(--fat-color) 75% 100%
            );
            margin: 0 auto;
            position: relative;
        }
        
        .macro-chart::before {
            content: "";
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 100px;
            height: 100px;
            background-color: white;
            border-radius: 50%;
        }
        
        .macro-legend {
            display: flex;
            justify-content: center;
            margin-top: 2rem;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            margin: 0 1rem;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 5px;
            margin-right: 0.5rem;
        }
        
        .protein-color {
            background-color: var(--protein-color);
        }
        
        .carbs-color {
            background-color: var(--carbs-color);
        }
        
        .fat-color {
            background-color: var(--fat-color);
        }
        
        .app-preview {
            background-color: var(--light-background);
        }
        
        .app-screenshots {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
        }
        
        .app-screenshot {
            width: 250px;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .app-screenshot:hover {
            transform: scale(1.05);
        }
        
        .testimonials {
            background-color: white;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .testimonial-card {
            background-color: var(--light-background);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1rem;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-image {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 1rem;
        }
        
        .pricing {
            background-color: var(--light-background);
        }
        
        .pricing-plans {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2rem;
        }
        
        .pricing-card {
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
            width: 300px;
            transition: transform 0.3s;
        }
        
        .pricing-card:hover {
            transform: translateY(-10px);
        }
        
        .pricing-card.featured {
            border: 2px solid var(--primary-color);
            position: relative;
        }
        
        .featured-label {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background-color: var(--primary-color);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        .price {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--primary-color);
            margin: 1rem 0;
        }
        
        .price span {
            font-size: 1rem;
            color: var(--light-text);
        }
        
        .pricing-features {
            list-style: none;
            margin: 2rem 0;
        }
        
        .pricing-features li {
            margin-bottom: 0.5rem;
            position: relative;
            padding-left: 1.5rem;
        }
        
        .pricing-features li::before {
            content: "✓";
            color: var(--primary-color);
            position: absolute;
            left: 0;
        }
        
        .cta {
            text-align: center;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1498837167922-ddd27525d352?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80' );
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 0;
        }
        
        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .cta p {
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        footer {
            background-color: var(--text-color);
            color: white;
            padding: 3rem 0;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        
        .footer-column {
            flex: 1;
            min-width: 200px;
            margin-bottom: 2rem;
        }
        
        .footer-column h3 {
            margin-bottom: 1rem;
            color: var(--accent-color);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.5rem;
        }
        
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            list-style: none;
        }
        
        .social-links li {
            margin-right: 1rem;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--accent-color);
        }
        
        .copyright {
            text-align: center;
            margin-top: 2rem;
            padding-top: 2rem;
            border-top: 1px solid #444;
            color: #ccc;
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .about-text, .formula-text {
                padding-right: 0;
                margin-bottom: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <div class="logo">Balance<span>Nutrition</span></div>
                <ul class="nav-links">
                    <li><a href="#about">About</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#how-it-works">How It Works</a></li>
                    <li><a href="#formula">Our Formula</a></li>
                    <li><a href="#app">App</a></li>
                    <li><a href="#pricing">Pricing</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Achieve Your Weight Loss Goals Through Balanced Nutrition</h1>
                <p>Our personalized approach tailors balanced meals to your individual weight, helping you lose weight naturally and sustainably.</p>
                <a href="#pricing" class="btn">Get Started Today</a>
            </div>
        </div>
    </section>

    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About Us</h2>
                <p>We're on a mission to transform how people approach weight loss through balanced nutrition.</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Our Approach to Weight Loss</h3>
                    <p>At BalanceNutrition, we believe that sustainable weight loss comes from balanced eating, not restrictive dieting. Our approach is based on scientific research showing that weight management is most effective when meals are properly balanced between carbohydrates, protein, fiber, and healthy fats.</p>
                    <p>Unlike one-size-fits-all diets, our system is tailored to your individual weight, metabolism, and activity level, creating a personalized nutrition plan that works specifically for you.</p>
                    <p>We combine the best aspects of proven weight loss models with cutting-edge nutritional science to create a system that's both effective and sustainable for long-term results.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1505576399279-565b52d4ac71?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Balanced meal preparation">
                </div>
            </div>
        </div>
    </section>

    <section id="features" class="features">
        <div class="container">
            <div class="section-title">
                <h2>Key Features</h2>
                <p>Discover what makes our approach to weight loss unique and effective.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">⚖️</div>
                    <h3>Personalized Meal Formula</h3>
                    <p>Our proprietary formula creates meal plans tailored specifically to your weight, age, gender, and activity level for optimal results.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🥗</div>
                    <h3>Balanced Macronutrients</h3>
                    <p>We ensure the perfect balance of carbs, protein, fiber, and healthy fats in every meal to support weight loss and overall health.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⏰</div>
                    <h3>Strategic Meal Timing</h3>
                    <p>Our system optimizes when you eat, not just what you eat, to maximize metabolism and energy throughout the day.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📱</div>
                    <h3>Mobile App Guidance</h3>
                    <p>Our intuitive app makes following your personalized plan simple with meal tracking, progress monitoring, and educational resources.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🔍</div>
                    <h3>Progress Tracking</h3>
                    <p>Visualize your journey with comprehensive tracking of weight, measurements, and nutritional adherence.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🧠</div>
                    <h3>Nutritional Education</h3>
                    <p>Learn the science behind balanced nutrition so you can make informed choices for lifelong health.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="how-it-works" class="how-it-works">
        <div class="container">
            <div class="section-title">
                <h2>How It Works</h2>
                <p>Our simple process helps you achieve your weight loss goals through personalized nutrition.</p>
            </div>
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Personal Assessment</h3>
                    <p>Complete a comprehensive assessment of your weight, height, age, activity level, and dietary preferences.</p>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>Personalized Plan</h3>
                    <p>Receive your custom nutrition plan with balanced meals tailored to your specific weight and goals.</p>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>Follow Your Plan</h3>
                    <p>Use our app to track meals, monitor portions, and stay accountable to your personalized plan.</p>
                </div>
                <div class="step">
                    <div class="step-number">4</div>
                    <h3>Track Progress</h3>
                    <p>Monitor your weight loss journey with comprehensive tracking tools and regular progress updates.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="formula" class="nutrition-formula">
        <div class="container">
            <div class="section-title">
                <h2>Our Personalized Formula</h2>
                <p>The science behind our balanced nutrition approach to weight loss.</p>
            </div>
            <div class="formula-content">
                <div class="formula-text">
                    <h3>Science-Based Nutrition</h3>
                    <p>Our personalized meal formula is based on extensive research in nutritional science and metabolism. We calculate your Basal Metabolic Rate (BMR ) and Total Daily Energy Expenditure (TDEE) to determine your optimal calorie intake for weight loss.</p>
                    <p>The formula then distributes those calories across macronutrients in the ideal ratio for your body: 25-35% protein to preserve muscle mass, 40-50% complex carbohydrates for sustained energy, and 20-30% healthy fats for hormone balance and satiety.</p>
                    <p>We further personalize your plan based on your weight category, activity level, and age, ensuring that your nutrition plan is perfectly tailored to your individual needs.</p>
                    <p>The result is a balanced approach to eating that creates a moderate calorie deficit while ensuring nutritional adequacy, leading to sustainable weight loss without hunger or deprivation.</p>
                </div>
                <div class="formula-chart">
                    <div class="macro-chart"></div>
                    <div class="macro-legend">
                        <div class="legend-item">
                            <div class="legend-color protein-color"></div>
                            <span>Protein (30%)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color carbs-color"></div>
                            <span>Carbs (45%)</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color fat-color"></div>
                            <span>Fat (25%)</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="app" class="app-preview">
        <div class="container">
            <div class="section-title">
                <h2>Our Mobile App</h2>
                <p>Your personal nutrition coach in your pocket.</p>
            </div>
            <div class="app-screenshots">
                <img src="https://cdn.dribbble.com/users/1615584/screenshots/15571949/media/7e95f0fddb7957220033569815885822.jpg?compress=1&resize=1000x750" alt="App Dashboard" class="app-screenshot">
                <img src="https://cdn.dribbble.com/users/1615584/screenshots/15571949/media/de37774c651d06af83e7be4aa1a87826.jpg?compress=1&resize=1000x750" alt="Meal Planning" class="app-screenshot">
                <img src="https://cdn.dribbble.com/users/1615584/screenshots/15571949/media/a12a01aad39b76d6c78941773ef742b5.jpg?compress=1&resize=1000x750" alt="Progress Tracking" class="app-screenshot">
            </div>
        </div>
    </section>

    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Success Stories</h2>
                <p>Hear from people who have transformed their lives with our balanced nutrition approach.</p>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "I've tried countless diets before, but this is the first approach that actually feels sustainable. I've lost 15 pounds in 2 months without feeling deprived or hungry. The personalized meal plans make all the difference!"
                    </div>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/women/45.jpg" alt="Sarah J." class="author-image">
                        <div>
                            <h4>Sarah J.</h4>
                            <p>Lost 15 lbs in 2 months</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "As a busy professional, I never had time to figure out proper nutrition. This app makes it so easy with personalized meal suggestions and simple tracking. I've lost weight steadily and have so much more energy throughout the day."
                    </div>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Michael T." class="author-image">
                        <div>
                            <h4>Michael T.</h4>
                            <p>Lost 22 lbs in 3 months</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "The educational aspect of this program is what sets it apart. I'm not just losing weight, I'm learning about nutrition and how my body works. For the first time, I feel like I have the knowledge to maintain my weight loss long-term."
                    </div>
                    <div class="testimonial-author">
                        <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Jennifer R." class="author-image">
                        <div>
                            <h4>Jennifer R.</h4>
                            <p>Lost 30 lbs in 4 months</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="pricing" class="pricing">
        <div class="container">
            <div class="section-title">
                <h2>Pricing Plans</h2>
                <p>Choose the plan that fits your needs and start your weight loss journey today.</p>
            </div>
            <div class="pricing-plans">
                <div class="pricing-card">
                    <h3>Basic</h3>
                    <div class="price">$4.99<span>/month</span></div>
                    <p>Perfect for beginners starting their weight loss journey.</p>
                    <ul class="pricing-features">
                        <li>Personalized meal formula</li>
                        <li>Basic meal tracking</li>
                        <li>Weight progress tracking</li>
                        <li>Standard food database</li>
                        <li>Educational articles</li>
                    </ul>
                    <a href="#" class="btn">Get Started</a>
                </div>
                <div class="pricing-card featured">
                    <div class="featured-label">Most Popular</div>
                    <h3>Premium</h3>
                    <div class="price">$9.99<span>/month</span></div>
                    <p>Enhanced features for optimal weight loss results.</p>
                    <ul class="pricing-features">
                        <li>Everything in Basic</li>
                        <li>Advanced analytics</li>
                        <li>Customized meal plans</li>
                        <li>Recipe suggestions</li>
                        <li>Body measurement tracking</li>
                        <li>Progress photos</li>
                        <li>Community access</li>
                    </ul>
                    <a href="#" class="btn">Get Started</a>
                </div>
                <div class="pricing-card">
                    <h3>Family</h3>
                    <div class="price">$19.99<span>/month</span></div>
                    <p>Perfect for households working toward health goals together.</p>
                    <ul class="pricing-features">
                        <li>Everything in Premium</li>
                        <li>Up to 5 user profiles</li>
                        <li>Family meal planning</li>
                        <li>Shared grocery lists</li>
                        <li>Family challenges</li>
                        <li>Priority support</li>
                    </ul>
                    <a href="#" class="btn">Get Started</a>
                </div>
            </div>
        </div>
    </section>

    <section class="cta">
        <div class="container">
            <h2>Start Your Weight Loss Journey Today</h2>
            <p>Join thousands of people who have transformed their lives through our balanced nutrition approach to weight loss.</p>
            <a href="#pricing" class="btn">Get Started Now</a>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>BalanceNutrition</h3>
                    <p>Personalized weight loss through balanced nutrition, tailored to your individual needs.</p>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#how-it-works">How It Works</a></li>
                        <li><a href="#formula">Our Formula</a></li>
                        <li><a href="#app">App</a></li>
                        <li><a href="#pricing">Pricing</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Legal</h3>
                    <ul class="footer-links">
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Cookie Policy</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Connect With Us</h3>
                    <ul class="social-links">
                        <li><a href="#">Facebook</a></li>
                        <li><a href="#">Twitter</a></li>
                        <li><a href="#">Instagram</a></li>
                        <li><a href="#">LinkedIn</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 BalanceNutrition. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
