# activity

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MVM School - Quality Education for All</title>
    
    <style>
        /* ==========================================
           GLOBAL STYLES AND RESET
           ========================================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f4f4f4;
        }

        /* ==========================================
           HEADER AND NAVIGATION STYLES
           ========================================== */
        header {
            background: linear-gradient(135deg, #0066cc 0%, #004499 100%);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            z-index: 100;
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .school-name {
            font-size: 1.8rem;
            font-weight: bold;
            text-decoration: none;
            color: white;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
            border-bottom: 2px solid transparent;
        }

        nav a:hover {
            border-bottom-color: #ffeb3b;
            transform: translateY(-2px);
        }

        /* ==========================================
           MAIN CONTAINER AND SECTIONS
           ========================================== */
        main {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            margin: 3rem 0;
            padding: 2rem;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            color: #0066cc;
            margin-bottom: 1rem;
            font-size: 2rem;
            text-align: center;
        }

        h2 {
            color: #0066cc;
            margin-bottom: 1rem;
            font-size: 1.8rem;
            border-bottom: 3px solid #0066cc;
            padding-bottom: 0.5rem;
        }

        h3 {
            color: #004499;
            margin: 1rem 0 0.5rem 0;
        }

        /* ==========================================
           HOME SECTION STYLES
           ========================================== */
        #home {
            text-align: center;
        }

        .banner {
            width: 100%;
            height: 300px;
            background: linear-gradient(135deg, #0066cc 0%, #00a8ff 100%);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 2rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .welcome-message {
            font-size: 1.2rem;
            color: #333;
            margin-bottom: 1rem;
            line-height: 1.8;
        }

        .welcome-btn {
            background-color: #0066cc;
            color: white;
            padding: 0.8rem 2rem;
            font-size: 1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 1rem;
            transition: all 0.3s ease;
        }

        .welcome-btn:hover {
            background-color: #004499;
            transform: scale(1.05);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .welcome-btn:active {
            transform: scale(0.98);
        }

        /* ==========================================
           ABOUT SECTION STYLES
           ========================================== */
        #about p {
            margin-bottom: 1rem;
            line-height: 1.8;
            text-align: justify;
        }

        .about-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .feature-box {
            background-color: #f0f8ff;
            padding: 1.5rem;
            border-radius: 8px;
            border-left: 4px solid #0066cc;
            transition: all 0.3s ease;
        }

        .feature-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 12px rgba(0, 102, 204, 0.2);
        }

        .feature-box h4 {
            color: #0066cc;
            margin-bottom: 0.5rem;
        }

        /* ==========================================
           COURSES SECTION STYLES
           ========================================== */
        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .course-card {
            background: linear-gradient(135deg, #f0f8ff 0%, #e6f2ff 100%);
            border: 2px solid #0066cc;
            border-radius: 8px;
            padding: 1.5rem;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .course-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 16px rgba(0, 102, 204, 0.3);
            border-color: #004499;
        }

        .course-card h3 {
            color: #0066cc;
            margin-top: 0;
        }

        .course-card p {
            font-size: 0.95rem;
            color: #555;
            margin-bottom: 1rem;
        }

        .course-badge {
            display: inline-block;
            background-color: #0066cc;
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: bold;
        }

        /* ==========================================
           CONTACT SECTION STYLES
           ========================================== */
        .contact-form {
            max-width: 500px;
            margin: 2rem auto;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-weight: 600;
            color: #0066cc;
            margin-bottom: 0.5rem;
        }

        .form-group input,
        .form-group textarea {
            padding: 0.8rem;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #0066cc;
            box-shadow: 0 0 5px rgba(0, 102, 204, 0.3);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .submit-btn {
            background-color: #0066cc;
            color: white;
            padding: 0.8rem 2rem;
            font-size: 1rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            align-self: center;
            margin-top: 0.5rem;
        }

        .submit-btn:hover {
            background-color: #004499;
            transform: scale(1.05);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .submit-btn:active {
            transform: scale(0.98);
        }

        /* Error message styling */
        .error-message {
            color: #d32f2f;
            font-size: 0.85rem;
            margin-top: 0.3rem;
            display: none;
        }

        .error-message.show {
            display: block;
        }

        .form-group.error input,
        .form-group.error textarea {
            border-color: #d32f2f;
            background-color: #ffebee;
        }

        /* ==========================================
           FOOTER STYLES
           ========================================== */
        footer {
            background-color: #0066cc;
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            border-top: 4px solid #004499;
        }

        footer p {
            margin: 0;
        }

        /* ==========================================
           RESPONSIVE DESIGN (MOBILE SCREENS)
           ========================================== */
        @media (max-width: 768px) {
            /* Navigation adjustment for mobile */
            nav ul {
                flex-direction: column;
                gap: 0.5rem;
            }

            nav a {
                display: block;
                padding: 0.5rem;
            }

            /* Heading adjustments */
            h1 {
                font-size: 1.5rem;
            }

            h2 {
                font-size: 1.4rem;
            }

            /* Banner adjustment */
            .banner {
                height: 200px;
                font-size: 1.5rem;
            }

            /* Grid adjustments */
            .courses-grid {
                grid-template-columns: 1fr;
            }

            .about-features {
                grid-template-columns: 1fr;
            }

            /* Header container adjustment */
            .header-container {
                flex-direction: column;
                gap: 1rem;
                text-align: center;
            }

            /* Form adjustment */
            .contact-form {
                max-width: 100%;
            }

            /* Section padding */
            section {
                padding: 1.5rem;
                margin: 2rem 0;
            }
        }

        @media (max-width: 480px) {
            .school-name {
                font-size: 1.3rem;
            }

            nav ul {
                gap: 0.3rem;
            }

            nav a {
                font-size: 0.9rem;
            }

            h1 {
                font-size: 1.2rem;
            }

            h2 {
                font-size: 1.1rem;
            }

            .banner {
                height: 150px;
                font-size: 1.2rem;
            }

            .welcome-message {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- ==========================================
         HEADER WITH NAVIGATION
         ========================================== -->
    <header>
        <div class="header-container">
            <h1 class="school-name">📚 MVM School</h1>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#courses">Courses</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- ==========================================
         MAIN CONTENT
         ========================================== -->
    <main>
        <!-- HOME SECTION -->
        <section id="home">
            <div class="banner">
                🎓 Welcome to MVM School
            </div>
            <h1>Quality Education for All</h1>
            <p class="welcome-message">
                Welcome to MVM School, where we believe in providing quality education
                to all students. Our dedicated teachers and modern facilities ensure that
                every student gets the best learning experience possible.
            </p>
            <button class="welcome-btn" onclick="showWelcomeMessage()">
                ✨ Click to Explore!
            </button>
        </section>

        <!-- ABOUT SECTION -->
        <section id="about">
            <h2>About Our School</h2>
            <p>
                MVM School has been serving the community for over 20 years. We are committed
                to providing excellent education and nurturing the talents of every student.
                Our school offers a holistic approach to education, combining academics with
                extracurricular activities.
            </p>
            <p>
                With a team of experienced teachers and state-of-the-art facilities, we create
                an environment where students can learn, grow, and excel. We believe in fostering
                creativity, critical thinking, and character development in every student.
            </p>

            <!-- Features Section -->
            <div class="about-features">
                <div class="feature-box">
                    <h4>🎯 Expert Teachers</h4>
                    <p>
                        Our team consists of highly qualified and experienced educators who are
                        passionate about teaching and student development.
                    </p>
                </div>
                <div class="feature-box">
                    <h4>🏫 Modern Facilities</h4>
                    <p>
                        From science laboratories to computer labs, we have all the facilities
                        needed for comprehensive learning.
                    </p>
                </div>
                <div class="feature-box">
                    <h4>🌟 Student Growth</h4>
                    <p>
                        We focus on overall development of students including academics,
                        sports, and co-curricular activities.
                    </p>
                </div>
            </div>
        </section>

        <!-- COURSES SECTION -->
        <section id="courses">
            <h2>Our Courses</h2>
            <div class="courses-grid">
                <!-- Course 1 -->
                <div class="course-card">
                    <h3>📐 Mathematics</h3>
                    <p>
                        Master the fundamentals and advanced concepts of mathematics including
                        algebra, geometry, trigonometry, and calculus.
                    </p>
                    <span class="course-badge">Grades 1-12</span>
                </div>

                <!-- Course 2 -->
                <div class="course-card">
                    <h3>🔬 Science</h3>
                    <p>
                        Explore the fascinating world of science through hands-on experiments
                        and practical learning in physics, chemistry, and biology.
                    </p>
                    <span class="course-badge">Grades 1-12</span>
                </div>

                <!-- Course 3 -->
                <div class="course-card">
                    <h3>🌍 English</h3>
                    <p>
                        Develop excellent communication skills through literature, grammar,
                        writing, and public speaking programs.
                    </p>
                    <span class="course-badge">Grades 1-12</span>
                </div>

                <!-- Course 4 -->
                <div class="course-card">
                    <h3>💻 Computer Science</h3>
                    <p>
                        Learn programming, web development, and digital skills to prepare
                        for the modern technological world.
                    </p>
                    <span class="course-badge">Grades 6-12</span>
                </div>

                <!-- Course 5 -->
                <div class="course-card">
                    <h3>🎨 Arts & Crafts</h3>
                    <p>
                        Express creativity through painting, drawing, sculpture, and other
                        artistic mediums.
                    </p>
                    <span class="course-badge">Grades 1-12</span>
                </div>

                <!-- Course 6 -->
                <div class="course-card">
                    <h3>⚽ Physical Education</h3>
                    <p>
                        Build fitness and teamwork skills through various sports and
                        physical activities.
                    </p>
                    <span class="course-badge">Grades 1-12</span>
                </div>
            </div>
        </section>

        <!-- CONTACT SECTION -->
        <section id="contact">
            <h2>Contact Us</h2>
            <p style="text-align: center; color: #666; margin-bottom: 1rem;">
                Have a question? We'd love to hear from you. Fill out the form below and
                we'll get back to you as soon as possible!
            </p>

            <form class="contact-form" onsubmit="validateAndSubmitForm(event)">
                <!-- Name Field -->
                <div class="form-group">
                    <label for="name">Your Name *</label>
                    <input 
                        type="text" 
                        id="name" 
                        name="name" 
                        placeholder="Enter your full name"
                        required
                    >
                    <span class="error-message" id="nameError"></span>
                </div>

                <!-- Email Field -->
                <div class="form-group">
                    <label for="email">Your Email *</label>
                    <input 
                        type="email" 
                        id="email" 
                        name="email" 
                        placeholder="Enter your email address"
                        required
                    >
                    <span class="error-message" id="emailError"></span>
                </div>

                <!-- Message Field -->
                <div class="form-group">
                    <label for="message">Your Message *</label>
                    <textarea 
                        id="message" 
                        name="message" 
                        placeholder="Enter your message here..."
                        required
                    ></textarea>
                    <span class="error-message" id="messageError"></span>
                </div>

                <!-- Submit Button -->
                <button type="submit" class="submit-btn">Send Message</button>
            </form>
        </section>
    </main>

    <!-- ==========================================
         FOOTER
         ========================================== -->
    <footer>
        <p>&copy; 2026 MVM School. All rights reserved. | Promoting Quality Education</p>
    </footer>

    <!-- ==========================================
         JAVASCRIPT - INTERACTIVE FEATURES
         ========================================== -->
    <script>
        // ==========================================
        // FUNCTION: Show Welcome Message
        // ==========================================
        // This function displays an alert when the
        // "Click to Explore!" button is clicked
        function showWelcomeMessage() {
            alert('🎉 Welcome to MVM School!\n\nWe are excited to have you here. Feel free to explore our courses and get in touch with us!');
        }

        // ==========================================
        // FUNCTION: Validate Email
        // ==========================================
        // This function checks if the email format
        // is valid using a regular expression
        function isValidEmail(email) {
            // Simple email validation pattern
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailPattern.test(email);
        }

        // ==========================================
        // FUNCTION: Clear Error Messages
        // ==========================================
        // This function removes error styling from
        // form fields and hides error messages
        function clearErrors() {
            // Get all form groups
            const formGroups = document.querySelectorAll('.form-group');
            
            // Remove error class from each group
            formGroups.forEach(group => {
                group.classList.remove('error');
            });

            // Hide all error messages
            const errorMessages = document.querySelectorAll('.error-message');
            errorMessages.forEach(message => {
                message.classList.remove('show');
            });
        }

        // ==========================================
        // FUNCTION: Show Error Message
        // ==========================================
        // This function displays an error message
        // for a specific form field
        function showError(fieldId, message) {
            // Get the form group containing this field
            const field = document.getElementById(fieldId);
            const formGroup = field.closest('.form-group');
            const errorElement = document.getElementById(fieldId + 'Error');

            // Add error styling
            formGroup.classList.add('error');
            errorElement.textContent = message;
            errorElement.classList.add('show');
        }

        // ==========================================
        // FUNCTION: Validate and Submit Form
        // ==========================================
        // This function validates the contact form
        // and shows appropriate error messages
        function validateAndSubmitForm(event) {
            // Prevent default form submission
            event.preventDefault();

            // Clear any previous errors
            clearErrors();

            // Get form field values
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();

            // Flag to track if form is valid
            let isValid = true;

            // ========== VALIDATION CHECKS ==========

            // Check if name is empty
            if (name === '') {
                showError('name', 'Please enter your name');
                isValid = false;
            }

            // Check if email is empty
            if (email === '') {
                showError('email', 'Please enter your email address');
                isValid = false;
            }
            // Check if email format is valid (only if not empty)
            else if (!isValidEmail(email)) {
                showError('email', 'Please enter a valid email address');
                isValid = false;
            }

            // Check if message is empty
            if (message === '') {
                showError('message', 'Please enter your message');
                isValid = false;
            }

            // ========== FORM SUBMISSION ==========

            // If all validations pass, show success message
            if (isValid) {
                // Show success alert
                alert(
                    '✅ Message Sent Successfully!\n\n' +
                    'Thank you for contacting us, ' + name + '!\n' +
                    'We will get back to you shortly at ' + email
                );

                // Reset the form to clear all fields
                document.querySelector('.contact-form').reset();

                // Optional: Clear focus from submit button
                document.activeElement.blur();
            }
        }

        // ==========================================
        // ADDITIONAL: Smooth Scrolling
        // ==========================================
        // This adds smooth scrolling when clicking
        // navigation links (modern browsers support this)
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
