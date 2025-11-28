<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إلى زوزايتي</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Tajawal', sans-serif;
            background-color: #ffe6e6;
            color: #4a4a4a;
            overflow-x: hidden;
            padding-bottom: 50px;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
        }

        /* تنسيق البطاقات */
        .card {
            background: white;
            border-radius: 20px;
            padding: 25px;
            margin-bottom: 20px;
            box-shadow: 0 4px 15px rgba(255, 105, 180, 0.2);
            text-align: center;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeIn 0.8s forwards;
        }
        
        /* تنسيق الصورة داخل البطاقة */
        .card img {
            max-width: 100%;
            height: auto;
            border-radius: 15px;
            margin-bottom: 15px;
        }

        /* تأخير ظهور الفقرات لجمالية أكثر */
        .card:nth-child(1) { animation-delay: 0.2s; }
        .card:nth-child(2) { animation-delay: 1.5s; }
        .card:nth-child(3) { animation-delay: 3s; }
        .card:nth-child(4) { animation-delay: 4.5s; }
        .card:nth-child(5) { animation-delay: 6s; }

        h1 {
            color: #ff4d6d;
            font-size: 24px;
            margin-bottom: 15px;
        }

        p {
            font-size: 18px;
            line-height: 1.6;
            margin-bottom: 10px;
        }

        .heart {
            color: #ff4d6d;
            font-size: 30px;
            margin: 10px 0;
        }

        /* تنسيق الشعر */
        .poem {
            font-weight: bold;
            color: #d63384;
            background-color: #fff0f5;
            padding: 15px;
            border-radius: 10px;
            border: 1px dashed #ff4d6d;
            margin: 15px 0;
        }

        /* تنسيق الأزرار */
        .buttons-container {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            margin-top: 20px;
            position: relative;
            height: 60px; /* مساحة لحركة الأزرار */
        }

        button {
            padding: 12px 30px;
            font-size: 18px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-family: 'Tajawal', sans-serif;
            font-weight: bold;
            transition: transform 0.2s;
        }

        .btn-yes {
            background-color: #ff4d6d;
            color: white;
            box-shadow: 0 4px 10px rgba(255, 77, 109, 0.4);
            z-index: 10;
        }

        .btn-no {
            background-color: #e0e0e0;
            color: #555;
            position: absolute; /* مهم للحركة */
            left: 20%; /* موقع مبدئي */
        }

        /* تأثير الظهور */
        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* رسالة القبول */
        #success-message {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 230, 230, 0.95);
            z-index: 100;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        
        #success-message h2 {
            font-size: 30px;
            color: #ff4d6d;
        }

        .floating-hearts {
            font-size: 50px;
            animation: pulse 1s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

    </style>
</head>
<body>

    <div class="container">
        <div class="card">
            <img src="9e034dd866d22d2ca42360b4d82f2bc7.jpg" alt="صورة لطيفة مع دب" style="max-width: 150px;">
            <h1>إلى زوزايتي 🌸</h1>
            <p>من أول يوم عرفتج بي، حسيت اكو شي تغير بحياتي. صرت أشوف الدنيا أحلى، والأيام اللي كانت عادية صارت وياج عيد.</p>
        </div>

        <div class="card">
            <img src="images (1).jfif" alt="صورة Hello Kitty مع قلوب" style="max-width: 120px;">
            <div class="heart">❤️</div>
            <p>ضحكتج صارت هي الأغنية المفضلة عندي، وعيونج هي العالم اللي أضيع بي وألكَى نفسي بي بنفس الوقت. أنتي مو بس شخص عادي، أنتي النعمة اللي أدعي ربي يحفظها إلي.</p>
        </div>

        <div class="card">
            <img src="images.jfif" alt="صورة Hello Kitty مع هدية" style="max-width: 100px;">
            <p>وياج أحس بالأمان، أحس إني أكدر أكون على طبيعتي بدون خوف. كل كلمة حلوة منج تنطيني طاقة، وكل زعلة منج تكسر قلبي. أنتي صرتي جزء مني ومن روحي.</p>
        </div>

        <div class="card">
            <div class="heart">✨</div>
            <p>كنت خايف أحجي، بس خوفي من إني أخسرج أكبر من خوفي من الاعتراف. قلبي ملى من الحب وما عاد يكدر يسكت أكثر من هيج.</p>
        </div>

        <div class="card">
            <h1>أحبج يا أغلى شي</h1>
            <p>أريد أكلج شي بقلبي من زمان..</p>
            
            <div class="poem">
                "يا أجمل الصدف يا أحلى أقداري<br>
                حبج سكن بالروح وغير أفكاري<br>
                أنتِ النبض للقلب وأنتِ الهوا للصدار<br>
                فدوا أروحلج يا زوزايتي يا نوري ونهاري"
            </div>

            <p style="margin-top: 15px; font-weight: bold;">تقبلين تكملين حياتج وياي؟ وتصيرين حبيبتي؟</p>

            <div class="buttons-container">
                <button class="btn-yes" onclick="showLove()">أكيد أقبل أحبك! 😍</button>
                <button class="btn-no" id="noBtn" onmouseover="moveButton()" ontouchstart="moveButton()">لا ما أريد 😒</button>
            </div>
        </div>
    </div>

    <div id="success-message">
        <div class="floating-hearts">❤️❤️❤️</div>
        <br>
        <h2>وأني أموت عليج! 💍</h2>
        <p>أسعد إنسان بالدنيا آني اليوم</p>
        <p>أحبج زوزايتي</p>
        <div class="floating-hearts">❤️❤️❤️</div>
    </div>

    <script>
        // دالة تحريك الزر "لا"
        function moveButton() {
            var btnNo = document.getElementById('noBtn');
            // حركة عشوائية للزر داخل مساحة الأزرار المخصصة له
            var randomX = Math.floor(Math.random() * 200) - 100;
            var randomY = Math.floor(Math.random() * 100) - 50;
            
            // يجعل الزر يقفز إلى مكان عشوائي قريب
            btnNo.style.transform = `translate(${randomX}px, ${randomY}px)`;
        }

        // دالة الضغط على "نعم"
        function showLove() {
            document.getElementById('success-message').style.display = 'flex';
            document.body.style.overflow = 'hidden'; // لإخفاء التمرير بعد القبول
        }
    </script>
</body>
</html>
