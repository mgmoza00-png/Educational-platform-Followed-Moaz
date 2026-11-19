<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بوابة المراجعات الشاملة - معهد MCI | معاذ إيهاب</title>
    <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
    <style>
        * { box-sizing: border-box; }
        body {
            font-family: 'Tahoma', sans-serif;
            margin: 0;
            min-height: 100vh;
            color: #ffffff;
            background-color: #000000;
        }

        /* --- الصفحة الأولى: شاشة تسجيل الدخول بخلفية باتمان كاملة --- */
        #loginSection {
            background: linear-gradient(rgba(0, 0, 0, 0.55), rgba(0, 0, 0, 0.72)), 
                        url('https://images.unsplash.com/photo-1509347528160-9a9e33742cdb?q=80&w=1920&auto=format&fit=crop') no-repeat center center fixed;
            background-size: cover;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }
        .card {
            background: rgba(10, 10, 14, 0.85);
            backdrop-filter: blur(8px);
            padding: 35px 25px;
            border-radius: 18px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.9);
            width: 100%;
            max-width: 440px;
            border: 1px solid rgba(250, 204, 21, 0.45);
            border-top: 6px solid #facc15;
        }
        h2 { text-align: center; color: #facc15; font-size: 22px; margin-bottom: 5px; font-weight: bold; }
        p.sub { text-align: center; color: #cbd5e1; font-size: 13px; margin-bottom: 20px; line-height: 1.6; }
        label { display: block; margin-bottom: 6px; font-size: 13px; font-weight: bold; color: #f1f5f9; }
        input {
            width: 100%;
            padding: 12px;
            margin-bottom: 16px;
            border: 1px solid #475569;
            border-radius: 10px;
            background: rgba(2, 6, 23, 0.9);
            color: #fff;
            font-size: 14px;
            transition: all 0.3s ease;
        }
        input:focus { outline: none; border-color: #facc15; box-shadow: 0 0 10px rgba(250, 204, 21, 0.5); }
        button {
            width: 100%;
            padding: 13px;
            background: linear-gradient(135deg, #ca8a04, #a16207);
            border: none;
            border-radius: 10px;
            color: #fff;
            font-weight: bold;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s;
            box-shadow: 0 4px 12px rgba(202, 138, 4, 0.4);
            margin-top: 5px;
        }
        button:hover { background: linear-gradient(135deg, #eab308, #ca8a04); transform: translateY(-1px); }
        button:disabled { background: #475569; cursor: not-allowed; transform: none; box-shadow: none; }
        .error-msg { color: #f87171; font-size: 12px; text-align: center; margin-bottom: 12px; display: none; font-weight: bold; }

        /* --- الصفحة الثانية: صفحة المراجعات بخلفية باتمان كاملة --- */
        #reviewsSection {
            display: none;
            background: linear-gradient(rgba(0, 0, 0, 0.60), rgba(0, 0, 0, 0.78)), 
                        url('https://images.unsplash.com/photo-1531259683007-016a7b628fc3?q=80&w=1920&auto=format&fit=crop') no-repeat center center fixed;
            background-size: cover;
            min-height: 100vh;
            padding: 30px 20px;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
        }
        header {
            text-align: center;
            margin-bottom: 30px;
            background: rgba(10, 10, 14, 0.85);
            backdrop-filter: blur(8px);
            padding: 20px;
            border-radius: 15px;
            border-top: 5px solid #facc15;
            box-shadow: 0 10px 30px rgba(0,0,0,0.8);
        }
        header h1 { color: #facc15; font-size: 24px; margin: 0 0 10px 0; }
        header p { color: #cbd5e1; font-size: 14px; margin: 0; }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 20px;
        }
        .subject-card {
            background: rgba(15, 15, 20, 0.86);
            backdrop-filter: blur(8px);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(250, 204, 21, 0.35);
            box-shadow: 0 8px 20px rgba(0,0,0,0.75);
            transition: 0.3s;
        }
        .subject-card:hover {
            transform: translateY(-5px);
            border-color: #facc15;
            box-shadow: 0 12px 25px rgba(250, 204, 21, 0.35);
        }
        .subject-card h3 { color: #facc15; margin-top: 0; font-size: 17px; border-bottom: 1px solid #334155; padding-bottom: 10px; }

        .btn-view {
            display: block;
            width: 100%;
            padding: 11px;
            background: linear-gradient(135deg, #ca8a04, #a16207);
            color: white;
            text-align: center;
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
            margin-top: 10px;
            font-size: 13px;
            transition: 0.3s;
        }
        .btn-view:hover { background: linear-gradient(135deg, #eab308, #ca8a04); }

        .footer-contact {
            margin-top: 25px;
            text-align: center;
            background: rgba(10, 10, 14, 0.88);
            padding: 16px;
            border-radius: 14px;
            border: 1px solid rgba(250, 204, 21, 0.35);
        }
        .footer-contact a {
            color: #facc15;
            font-weight: bold;
            text-decoration: none;
            font-size: 15px;
        }
        .footer-contact a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <!-- الصفحة الأولى: شاشة تسجيل الدخول -->
    <div id="loginSection">
        <div class="card">
            <h2>معهد MCI للعلوم الإدارية</h2>
            <p class="sub">إعداد الطالب: معاذ إيهاب<br>أدخل بياناتك وكلمة السر للوصول إلى المراجعات</p>

            <div id="errorBox" class="error-msg">عذراً، كلمة السر غير صحيحة! يرجى المحاولة مرة أخرى.</div>

            <form id="accessForm">
                <label>الاسم بالكامل:</label>
                <input type="text" id="student_name" required placeholder="اكتب اسمك ثلاثي">

                <label>الشعبة:</label>
                <input type="text" id="student_section" required placeholder="مثال: نظم معلومات / إدارة">

                <label>الكود الأكاديمي:</label>
                <input type="text" id="student_code" required placeholder="اكتب الكود الخاص بك">

                <label>كلمة السر الخاصة بالملفات:</label>
                <input type="password" id="access_password" required placeholder="أدخل كلمة السر">

                <button type="submit" id="submitBtn">فتح المراجعات</button>
            </form>

            <div class="footer-contact">
                <a href="https://wa.me/201033942182" target="_blank" rel="noopener noreferrer">تواصل عبر واتساب: +201033942182</a>
            </div>
        </div>
    </div>

    <!-- الصفحة الثانية: صفحة المراجعات -->
    <div id="reviewsSection">
        <div class="container">
            <header>
                <h1>معهد MCI للعلوم الإدارية - بوابة المراجعات الشاملة</h1>
                <p>إعداد الطالب: معاذ إيهاب | تصفح الشروحات وبنوك الأسئلة مباشرة</p>
            </header>

            <div class="grid">

                <!-- 1. مبادئ إدارة الأعمال -->
                <div class="subject-card">
                    <h3>📊 مبادئ إدارة الأعمال</h3>
                    <a href="https://www.mediafire.com/file/vml8hz40ahllt7d/المراجعة_النهائية_الشاملة_مبادئ_الإدارة_محمي_v2_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('المراجعة النهائية الشاملة - مبادئ الإدارة')">📄 فتح الشرح الشامل (MediaFire PDF)</a>
                    <a href="https://www.mediafire.com/file/jv2wv83z2r88bb0/بنك_الأسئلة_الشامل_75_سؤال_مبادئ_الإدارة_محمي_v2(1)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('بنك الأسئلة 75 سؤال - مبادئ الإدارة')">❓ فتح بنك الأسئلة 75 سؤالاً (MediaFire PDF)</a>
                </div>

                <!-- 2. مبادئ الاقتصاد -->
                <div class="subject-card">
                    <h3>📈 مبادئ الاقتصاد</h3>
                    <a href="https://www.mediafire.com/file/oqh5m56rt4zyv8t/الشرح_الشامل_مبادئ_الاقتصاد_محمي(1)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('الشرح الشامل - مبادئ الاقتصاد')">📄 فتح الشرح الشامل (MediaFire PDF)</a>
                    <a href="https://www.mediafire.com/file/3975vmsqs3z74g3/بنك_75_سؤال_مبادئ_الاقتصاد_محمي(1)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('بنك 75 سؤال - مبادئ الاقتصاد')">❓ فتح بنك الأسئلة 75 سؤالاً (MediaFire PDF)</a>
                </div>

                <!-- 3. أصول العلوم السياسية -->
                <div class="subject-card">
                    <h3>🏛️ أصول العلوم السياسية</h3>
                    <a href="https://www.mediafire.com/file/xto4butux9y97rv/الشرح_الشامل_أصول_العلوم_السياسية_محمي_v2(2)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('الشرح الشامل - أصول العلوم السياسية')">📄 فتح الشرح الشامل (MediaFire PDF)</a>
                    <a href="https://www.mediafire.com/file/dkyemivh0ebsz8z/بنك_75_سؤال_أصول_العلوم_السياسية_محمي_v2(2)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('بنك 75 سؤال - أصول العلوم السياسية')">❓ فتح بنك الأسئلة 75 سؤالاً (MediaFire PDF)</a>
                </div>

                <!-- 4. مبادئ القانون -->
                <div class="subject-card">
                    <h3>⚖️ مبادئ القانون</h3>
                    <a href="https://www.mediafire.com/file/6x9bbayubg4eqhf/الشرح_الشامل_المدخل_للعلوم_القانونية_محمي(1)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('الشرح الشامل - المدخل للعلوم القانونية')">📄 فتح الشرح الشامل (MediaFire PDF)</a>
                    <a href="https://www.mediafire.com/file/ul0fkzoggaq666g/بنك_75_سؤال_المدخل_للعلوم_القانونية_محمي(1)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('بنك 75 سؤال - المدخل للعلوم القانونية')">❓ فتح بنك الأسئلة 75 سؤالاً (MediaFire PDF)</a>
                </div>

                <!-- 5. مراسلات الأعمال -->
                <div class="subject-card">
                    <h3>🇬🇧 مراسلات الأعمال (Business English)</h3>
                    <a href="https://www.mediafire.com/file/zxr4an8qaasa96x/Business_Communication_Full_Explanation_Moaz-v3(1)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('Business Communication Full Explanation')">📄 فتح الشرح الشامل (MediaFire PDF)</a>
                    <a href="https://www.mediafire.com/file/k3sec7zg75noyg6/Business_Communication_75_Questions_Bank_Moaz-v3(1)_unlocked.pdf/file" class="btn-view" target="_blank" rel="noopener noreferrer" onclick="trackFileAccess('Business Communication 75 Questions Bank')">❓ فتح بنك الأسئلة 75 سؤالاً (MediaFire PDF)</a>
                </div>

            </div>

            <div class="footer-contact">
                <a href="https://wa.me/201033942182" target="_blank" rel="noopener noreferrer">تواصل عبر واتساب: +201033942182</a>
            </div>
        </div>
    </div>

    <script>
        try {
            emailjs.init("YOUR_PUBLIC_KEY");
        } catch(e) {}

        let currentStudent = {
            name: "",
            section: "",
            code: ""
        };

        function trackFileAccess(fileName) {
            const params = {
                to_email: "Mgmoza00@gmail.com",
                student_name: currentStudent.name || "غير مسجل",
                student_section: currentStudent.section || "غير مسجل",
                student_code: currentStudent.code || "غير مسجل",
                accessed_file: fileName
            };
            try {
                emailjs.send("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", params);
            } catch(e) {}
        }

        document.getElementById('accessForm').addEventListener('submit', function(event) {
            event.preventDefault();

            const passwordInput = document.getElementById('access_password').value;
            const errorBox = document.getElementById('errorBox');

            if (passwordInput !== "271017") {
                errorBox.style.display = "block";
                return;
            }

            errorBox.style.display = "none";
            const btn = document.getElementById('submitBtn');
            btn.disabled = true;
            btn.innerText = "جاري الدخول...";

            currentStudent = {
                name: document.getElementById('student_name').value,
                section: document.getElementById('student_section').value,
                code: document.getElementById('student_code').value
            };

            const templateParams = {
                to_email: "Mgmoza00@gmail.com",
                student_name: currentStudent.name,
                student_section: currentStudent.section,
                student_code: currentStudent.code,
                accessed_file: "دخول البوابة الرئيسية"
            };

            try {
                emailjs.send("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", templateParams)
                    .then(function() {
                        document.getElementById('loginSection').style.display = 'none';
                        document.getElementById('reviewsSection').style.display = 'block';
                    }, function(error) {
                        document.getElementById('loginSection').style.display = 'none';
                        document.getElementById('reviewsSection').style.display = 'block';
                    });
            } catch(err) {
                document.getElementById('loginSection').style.display = 'none';
                document.getElementById('reviewsSection').style.display = 'block';
            }
        });
    </script>
</body>
</html>
