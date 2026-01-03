<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HANDS‑ON | Practical Skills for Zambia</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background: #f5f5f5; color: #333; line-height: 1.6; }
        .container { max-width: 1200px; margin: 0 auto; padding: 20px; }
        header { background: linear-gradient(135deg, #1a5f23, #2e8b57); color: white; padding: 2rem; text-align: center; border-radius: 0 0 20px 20px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
        header h1 { font-size: 2.8rem; margin-bottom: 0.5rem; }
        header p { font-size: 1.2rem; opacity: 0.9; }
        .login-section, .main-app { background: white; border-radius: 15px; padding: 2rem; margin: 2rem auto; box-shadow: 0 6px 20px rgba(0,0,0,0.08); max-width: 500px; }
        .login-section h2, .main-app h2 { color: #2e8b57; margin-bottom: 1.5rem; text-align: center; }
        .form-group { margin-bottom: 1.5rem; }
        .form-group label { display: block; margin-bottom: 0.5rem; font-weight: 600; }
        .form-group input { width: 100%; padding: 12px; border: 2px solid #ddd; border-radius: 8px; font-size: 1rem; transition: border 0.3s; }
        .form-group input:focus { border-color: #2e8b57; outline: none; }
        .btn { display: block; width: 100%; background: #2e8b57; color: white; border: none; padding: 14px; border-radius: 8px; font-size: 1.1rem; font-weight: 600; cursor: pointer; transition: background 0.3s; }
        .btn:hover { background: #1a5f23; }
        .course-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 1.8rem; margin-top: 2rem; }
        .course-card { background: white; border-radius: 12px; padding: 1.8rem; box-shadow: 0 4px 10px rgba(0,0,0,0.05); border-left: 5px solid #2e8b57; transition: transform 0.3s; }
        .course-card:hover { transform: translateY(-5px); }
        .course-card h3 { color: #1a5f23; margin-bottom: 0.8rem; }
        .course-card p { font-size: 0.95rem; color: #666; margin-bottom: 1.2rem; }
        .resource-list { list-style: none; margin-bottom: 1.5rem; }
        .resource-list li { margin-bottom: 0.8rem; padding-left: 1.2rem; position: relative; }
        .resource-list li:before { content: '✓'; position: absolute; left: 0; color: #2e8b57; font-weight: bold; }
        .resource-list a { color: #2e8b57; text-decoration: none; font-weight: 600; border-bottom: 1px dotted #2e8b57; }
        .resource-list a:hover { border-bottom: 2px solid #2e8b57; }
        .cert-badge { display: inline-block; background: #ffeb3b; color: #333; font-size: 0.8rem; padding: 2px 8px; border-radius: 10px; margin-left: 0.5rem; font-weight: 600; }
        .hidden { display: none; }
        .logout { text-align: center; margin-top: 2rem; }
        .logout button { background: #ccc; color: #333; border: none; padding: 10px 20px; border-radius: 6px; cursor: pointer; }
        footer { text-align: center; margin-top: 3rem; padding: 1.5rem; color: #777; font-size: 0.9rem; border-top: 1px solid #eee; }
    </style>
</head>
<body>
    <header>
        <h1>HANDS‑ON</h1>
        <p>Practical skills for young Zambians</p>
    </header>

    <div class="container">
        <!-- Login Screen (initially visible) -->
        <section id="loginSection" class="login-section">
            <h2>Welcome to HANDS‑ON</h2>
            <form id="loginForm">
                <div class="form-group">
                    <label for="username">Username</label>
                    <input type="text" id="username" required placeholder="Enter your username">
                </div>
                <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" required placeholder="Enter your password">
                </div>
                <button type="submit" class="btn">Log In</button>
            </form>
            <p style="margin-top: 1rem; font-size: 0.9rem; color: #777; text-align: center;">
                First‑time users must use a provided username and password.
            </p>
        </section>

        <!-- Main App (hidden until login) -->
        <section id="mainApp" class="main-app hidden">
            <h2>Choose a Skill to Learn</h2>
            <div class="course-grid">
                <div class="course-card">
                    <h3>Agriculture & Farming</h3>
                    <p>Sustainable farming practices, crop management, and agri‑business.</p>
                    <ul class="resource-list">
                        <li><a href="http://www.fao.org/3/cb7051en/cb7051en.pdf" target="_blank">Save and Grow – A technical guide to agricultural practices in Zambia</a> (FAO)[reference:0]</li>
                        <li><a href="https://elearning.fao.org/" target="_blank">FAO elearning Academy</a> – Free certified courses in agriculture, food security, and more<span class="cert-badge">Certificate</span>[reference:1]</li>
                        <li><a href="https://www.saylor.org/" target="_blank">Saylor Academy</a> – Free courses with certificates in related subjects<span class="cert-badge">Certificate</span>[reference:2]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Construction & Carpentry</h3>
                    <p>Woodworking, roof framing, and general construction skills.</p>
                    <ul class="resource-list">
                        <li><a href="https://www.gutenberg.org/ebooks/70226" target="_blank">Carpentry by Ira Samuel Griffith</a> (Project Gutenberg)</li>
                        <li><a href="https://archive.org/details/bricklayingplast00hood" target="_blank">Bricklaying and Plastering</a> (Internet Archive)</li>
                        <li><a href="https://www.open.edu/openlearn/free-courses/full-catalogue" target="_blank">OpenLearn</a> – Free construction‑related courses<span class="cert-badge">Badge</span>[reference:3]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Tailoring & Fashion Design</h3>
                    <p>Garment construction, pattern making, and sewing techniques.</p>
                    <ul class="resource-list">
                        <li><a href="https://archive.org/download/stricklandatailoringmanual1956/stricklandatailoringmanual1956.pdf" target="_blank">A Tailoring Manual by Gertrude Strickland</a> (Internet Archive)</li>
                        <li><a href="https://www.saylor.org/" target="_blank">Saylor Academy</a> – Free professional development courses<span class="cert-badge">Certificate</span>[reference:4]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Metalwork & Welding</h3>
                    <p>Sheet‑metal work, welding, fabrication, and safety.</p>
                    <ul class="resource-list">
                        <li><a href="https://archive.org/details/metalfabrication0000ocon" target="_blank">Metal Fabrication: A Practical Guide</a> (Internet Archive)</li>
                        <li><a href="https://www.netacad.com/" target="_blank">Cisco Networking Academy</a> – Free courses in welding‑related technologies[reference:5]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Electrical & Electronics</h3>
                    <p>Wiring, circuit design, and electrical safety.</p>
                    <ul class="resource-list">
                        <li><a href="https://archive.org/details/electricalwiring00kemp" target="_blank">Electrical Wiring</a> (Public‑domain textbook)</li>
                        <li><a href="https://www.netacad.com/" target="_blank">Cisco Networking Academy</a> – Free networking and electronics courses[reference:6]</li>
                        <li><a href="https://learn.microsoft.com/" target="_blank">Microsoft Learn</a> – Free fundamental IT certifications<span class="cert-badge">Certificate</span>[reference:7]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Plumbing & Masonry</h3>
                    <p>Pipe fitting, masonry, and construction techniques.</p>
                    <ul class="resource-list">
                        <li><a href="https://archive.org/details/bricklayingplast00hood" target="_blank">Bricklaying and Plastering</a> (Internet Archive)</li>
                        <li><a href="https://www.open.edu/openlearn/free-courses/full-catalogue" target="_blank">OpenLearn</a> – Free courses on construction skills<span class="cert-badge">Badge</span>[reference:8]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Digital Literacy & IT</h3>
                    <p>Computer basics, coding, cybersecurity, and digital tools.</p>
                    <ul class="resource-list">
                        <li><a href="https://www.netacad.com/" target="_blank">Cisco Networking Academy</a> – Free courses in networking, cybersecurity, Python<span class="cert-badge">Certificate</span>[reference:9]</li>
                        <li><a href="https://grow.google/digitalgarage/" target="_blank">Google Digital Garage</a> – Free digital marketing and coding courses<span class="cert-badge">Certificate</span>[reference:10]</li>
                        <li><a href="https://learn.microsoft.com/" target="_blank">Microsoft Learn</a> – Free training for Microsoft certifications<span class="cert-badge">Certificate</span>[reference:11]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Business & Entrepreneurship</h3>
                    <p>Business planning, marketing, finance, and startup skills.</p>
                    <ul class="resource-list">
                        <li><a href="https://www.saylor.org/" target="_blank">Saylor Academy</a> – Free business courses with certificates<span class="cert-badge">Certificate</span>[reference:12]</li>
                        <li><a href="https://www.open.edu/openlearn/free-courses/full-catalogue" target="_blank">OpenLearn</a> – Free courses on money, business, and career development<span class="cert-badge">Badge</span>[reference:13]</li>
                        <li><a href="https://grow.google/digitalgarage/" target="_blank">Google Digital Garage</a> – Free digital business courses<span class="cert-badge">Certificate</span>[reference:14]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Personal Development & Soft Skills</h3>
                    <p>Communication, teamwork, problem‑solving, and career readiness.</p>
                    <ul class="resource-list">
                        <li><a href="https://www.open.edu/openlearn/miscellaneous/career-ready-courses" target="_blank">OpenLearn Career Ready Courses</a> – Free soft‑skills courses<span class="cert-badge">Badge</span>[reference:15]</li>
                        <li><a href="https://www.saylor.org/" target="_blank">Saylor Academy</a> – Free professional development certificates<span class="cert-badge">Certificate</span>[reference:16]</li>
                    </ul>
                </div>
                <div class="course-card">
                    <h3>Health & Home Management</h3>
                    <p>Nutrition, home economics, and basic healthcare.</p>
                    <ul class="resource-list">
                        <li><a href="https://archive.org/details/homemanagementpr00patt" target="_blank">Home Management: Principles and Practices</a> (Internet Archive)</li>
                        <li><a href="https://elearning.fao.org/" target="_blank">FAO elearning Academy</a> – Free courses on nutrition and food safety<span class="cert-badge">Certificate</span>[reference:17]</li>
                    </ul>
                </div>
            </div>
            <div class="logout">
                <button id="logoutBtn">Log Out</button>
            </div>
        </section>
    </div>

    <footer>
        <p>HANDS‑ON &copy; 2026 | Designed for offline access. Internet required for course resources.</p>
        <p>All resources are free and from official, trustworthy platforms. Certificates are available where indicated.</p>
    </footer>

    <script>
        // Predefined credentials (25 usernames & passwords) – unchanged
        const credentials = [
            { user: "ZambiaSkill_9f3", pass: "7X#pL2q!R8" },
            { user: "LearnPractical_4b", pass: "K5$jH@9mN1" },
            { user: "HandsOn_22q", pass: "3f&8zQ*wP6" },
            { user: "YouthVocational_7t", pass: "9B#vR2s@L4" },
            { user: "SkillUp_5r", pass: "2Y!pK8#mN3" },
            { user: "CraftMaster_1x", pass: "6Z$jH4!qP9" },
            { user: "AgriLearn_8s", pass: "4M#rT2@kL7" },
            { user: "BuildZambia_3n", pass: "8V!pQ5#jH2" },
            { user: "TailorPro_6w", pass: "1X$kL9!mN4" },
            { user: "MetalWorks_2y", pass: "5P#jH3@qR8" },
            { user: "ElectricSkill_7u", pass: "3K!mN6#pL1" },
            { user: "BrickArt_4p", pass: "7Q$jH2!rT5" },
            { user: "HomeManage_9c", pass: "2N#pL8@kH4" },
            { user: "VocationalEdge_5d", pass: "6H!qR3#jM9" },
            { user: "PracticalPath_1v", pass: "9L$pK2!mN7" },
            { user: "SkillHub_8m", pass: "4R#jH5@qP3" },
            { user: "LearnByDoing_3a", pass: "8M!pL6#kH2" },
            { user: "ZambiaCraft_6b", pass: "1T$jH9!rQ4" },
            { user: "WorkshopPro_2e", pass: "5P#kL3@mN8" },
            { user: "FutureBuilder_7h", pass: "3Q!jH6#pL1" },
            { user: "AgriExpert_4k", pass: "7N$pK2!rT9" },
            { user: "TailorCraft_9d", pass: "2H#jL8@qP5" },
            { user: "MetalArt_5f", pass: "6M!pR3#kH4" },
            { user: "WireMaster_1g", pass: "9Q$jL2!mN7" },
            { user: "MasonPro_8j", pass: "4P#kH5@rT3" }
        ];

        // Login logic
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const username = document.getElementById('username').value.trim();
            const password = document.getElementById('password').value.trim();

            const valid = credentials.find(c => c.user === username && c.pass === password);
            if (valid) {
                document.getElementById('loginSection').classList.add('hidden');
                document.getElementById('mainApp').classList.remove('hidden');
            } else {
                alert('Invalid username or password. Please use a provided credential.');
            }
        });

        // Logout logic
        document.getElementById('logoutBtn').addEventListener('click', function() {
            document.getElementById('loginSection').classList.remove('hidden');
            document.getElementById('mainApp').classList.add('hidden');
            document.getElementById('username').value = '';
            document.getElementById('password').value = '';
        });
    </script>
</body>
</html>
