<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Land Survey Blog</title>
    <style>
        /* ---------- RESET & BASE ---------- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: #f5f2ed;
            color: #2c2c2c;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 24px;
            padding: 30px 25px;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.08);
        }

        /* ---------- HEADER ---------- */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            border-bottom: 2px solid #e8e0d8;
            padding-bottom: 18px;
            margin-bottom: 28px;
        }

        .logo h1 {
            font-size: 26px;
            color: #3a5e3a;
            letter-spacing: -0.5px;
        }

        .logo span {
            font-weight: 300;
            color: #7a9e7a;
        }

        nav a {
            margin-left: 18px;
            text-decoration: none;
            color: #3a5e3a;
            font-weight: 600;
            font-size: 15px;
            transition: 0.2s;
        }

        nav a:hover {
            color: #1f3a1f;
            text-decoration: underline;
        }

        /* ---------- BLOG POSTS ---------- */
        .post {
            background: #faf8f6;
            border-radius: 16px;
            padding: 20px 22px;
            margin-bottom: 24px;
            border-left: 5px solid #7a9e7a;
            transition: 0.2s;
        }

        .post:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.04);
        }

        .post h2 {
            font-size: 22px;
            color: #1f3a1f;
            margin-bottom: 6px;
        }

        .post .meta {
            font-size: 13px;
            color: #888;
            margin-bottom: 12px;
        }

        .post .meta span {
            background: #e8e0d8;
            padding: 2px 12px;
            border-radius: 30px;
            font-size: 12px;
            margin-left: 8px;
        }

        .post p {
            line-height: 1.7;
            color: #444;
            margin-bottom: 14px;
        }

        .post .actions {
            display: flex;
            align-items: center;
            gap: 18px;
        }

        .post .actions button {
            background: none;
            border: 1.5px solid #c5d6c5;
            padding: 6px 18px;
            border-radius: 40px;
            font-size: 14px;
            font-weight: 600;
            color: #3a5e3a;
            cursor: pointer;
            transition: 0.2s;
        }

        .post .actions button:hover {
            background: #3a5e3a;
            color: white;
            border-color: #3a5e3a;
        }

        .post .actions .likes {
            font-size: 14px;
            color: #555;
        }

        .post .actions .likes span {
            font-weight: 700;
            color: #1f3a1f;
        }

        /* ---------- CONTACT FORM ---------- */
        .contact-section {
            margin-top: 40px;
            padding-top: 28px;
            border-top: 2px solid #e8e0d8;
        }

        .contact-section h3 {
            font-size: 22px;
            color: #1f3a1f;
            margin-bottom: 18px;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .contact-form input,
        .contact-form textarea {
            padding: 12px 16px;
            border: 1.5px solid #dcd5cd;
            border-radius: 12px;
            font-size: 15px;
            transition: 0.2s;
            background: #faf8f6;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: #7a9e7a;
            box-shadow: 0 0 0 3px rgba(122, 158, 122, 0.15);
        }

        .contact-form textarea {
            height: 80px;
            resize: vertical;
        }

        .contact-form button {
            background: #3a5e3a;
            color: white;
            border: none;
            padding: 14px;
            border-radius: 40px;
            font-size: 17px;
            font-weight: 700;
            cursor: pointer;
            transition: 0.2s;
        }

        .contact-form button:hover {
            background: #1f3a1f;
            transform: scale(1.01);
        }

        #form-feedback {
            margin-top: 12px;
            font-weight: 600;
            color: #3a5e3a;
        }

        /* ---------- FOOTER ---------- */
        footer {
            margin-top: 30px;
            text-align: center;
            font-size: 14px;
            color: #999;
            border-top: 1px solid #e8e0d8;
            padding-top: 22px;
        }

        /* ---------- MOBILE ---------- */
        @media (max-width: 600px) {
            header {
                flex-direction: column;
                align-items: flex-start;
                gap: 12px;
            }

            nav a {
                margin-left: 0;
                margin-right: 16px;
                font-size: 14px;
            }

            .container {
                padding: 18px 14px;
            }

            .post h2 {
                font-size: 19px;
            }
        }
    </style>
</head>
<body>

    <div class="container">

        <!-- HEADER -->
        <header>
            <div class="logo">
                <h1>🌍 Survey<span>Blog</span></h1>
            </div>
            <nav>
                <a href="#">Home</a>
                <a href="#">Articles</a>
                <a href="#">About</a>
            </nav>
        </header>

        <!-- BLOG POSTS -->
        <div id="blog-posts">

            <!-- Post 1 -->
            <div class="post" data-id="1">
                <h2>How Drones Are Changing Land Surveys</h2>
                <div class="meta">📅 June 22, 2026 <span>Tech</span></div>
                <p>Drones equipped with LiDAR and high-res cameras can map 100 acres in under 30 minutes. This is cutting survey time by 70% and reducing human error. Surveyors are now able to access hard-to-reach terrain without risk.</p>
                <div class="actions">
                    <button class="like-btn">❤️ Like</button>
                    <span class="likes">👍 <span id="likes-1">12</span> people liked this</span>
                </div>
            </div>

            <!-- Post 2 -->
            <div class="post" data-id="2">
                <h2>Boundary Disputes? Here's What to Do</h2>
                <div class="meta">📅 June 18, 2026 <span>Legal</span></div>
                <p>Boundary conflicts are common in rural areas. The first step is always to get a licensed surveyor to re-establish the original markers. In Kenya, the Land Registration Act requires official documentation before any dispute goes to court.</p>
                <div class="actions">
                    <button class="like-btn">❤️ Like</button>
                    <span class="likes">👍 <span id="likes-2">8</span> people liked this</span>
                </div>
            </div>

            <!-- Post 3 -->
            <div class="post" data-id="3">
                <h2>Soil Quality Testing 101 for Farmers</h2>
                <div class="meta">📅 June 14, 2026 <span>Agriculture</span></div>
                <p>Before you plant, test your soil. pH levels, nitrogen, phosphorus, and potassium determine what crops will thrive. Many agricultural extensions offer free or low-cost testing kits. A proper survey of your land's soil can double your yield.</p>
                <div class="actions">
                    <button class="like-btn">❤️ Like</button>
                    <span class="likes">👍 <span id="likes-3">21</span> people liked this</span>
                </div>
            </div>

        </div>

        <!-- CONTACT SECTION -->
        <div class="contact-section">
            <h3>📬 Have a Survey Question?</h3>
            <form class="contact-form" id="contactForm">
                <input type="text" id="name" placeholder="Your Name" required>
                <input type="email" id="email" placeholder="Your Email" required>
                <textarea id="message" placeholder="Ask about land surveys, boundaries, or soil..." required></textarea>
                <button type="submit">Send Message</button>
            </form>
            <p id="form-feedback"></p>
        </div>

        <!-- FOOTER -->
        <footer>
            &copy; 2026 SurveyBlog — Built for land surveyors &amp; farmers
        </footer>

    </div>

    <!-- JAVASCRIPT -->
    <script>
        // ---------- LIKE BUTTONS (Local storage keeps likes even after refresh) ----------
        document.querySelectorAll('.like-btn').forEach(button => {
            button.addEventListener('click', function() {
                // Find the post container
                const post = this.closest('.post');
                const postId = post.dataset.id;
                const likesSpan = document.getElementById(`likes-${postId}`);

                // Get current likes from localStorage or use the HTML value
                let currentLikes = parseInt(localStorage.getItem(`likes-${postId}`)) || parseInt(likesSpan.textContent);

                // Increase likes
                currentLikes += 1;
                likesSpan.textContent = currentLikes;
                localStorage.setItem(`likes-${postId}`, currentLikes);

                // Change button text temporarily
                this.textContent = '✅ Liked!';
                this.style.borderColor = '#3a5e3a';
                setTimeout(() => {
                    this.textContent = '❤️ Like';
                    this.style.borderColor = '#c5d6c5';
                }, 1500);
            });
        });

        // Load saved likes on page load
        document.querySelectorAll('.post').forEach(post => {
            const postId = post.dataset.id;
            const saved = localStorage.getItem(`likes-${postId}`);
            if (saved !== null) {
                document.getElementById(`likes-${postId}`).textContent = saved;
            }
        });

        // ---------- CONTACT FORM (Simulated submission) ----------
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();

            if (!name || !email || !message) {
                document.getElementById('form-feedback').textContent = '⚠️ Please fill in all fields.';
                document.getElementById('form-feedback').style.color = '#b33';
                return;
            }

            // Simulate sending (in reality, you'd connect to Formspree here)
            document.getElementById('form-feedback').textContent = '✅ Thanks, ' + name + '! Your question has been sent.';
            document.getElementById('form-feedback').style.color = '#3a5e3a';

            // Clear form
            this.reset();

            // Optional: Log to console (so you can see the data)
            console.log('Contact Form Data:', { name, email, message });
        });
    </script>

</body>
</html>