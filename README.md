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
            scroll-behavior: smooth; /* لتحريك الصفحة بسلاسة عند الضغط على استمرار */
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
        }

        /* تنسيق الفقرات التي يتم إخفائها */
        .hidden-content {
            display: none; /* إخفاء باقي الفقرات مبدئياً */
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 1s ease-in, transform 1s ease-in;
        }
        
        /* تنسيق الفقرات بعد الظهور */
        .show-content {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }

        /* تنسيق الصورة */
        .main-image {
            max-width: 150px;
            height: auto;
            border-radius: 50%;
            margin-bottom: 20px;
            border: 5px solid #ff4d6d;
        }

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

        /* تنسيق الأزرار (في الفقرة الأولى والأخيرة) */
        .buttons-container {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            margin-top: 20px;
            position: relative;
            height: 60px; 
        }

        button {
            padding: 12px 30px;
            font-size: 18px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-family: 'Tajawal', sans-serif;
            font-weight: bold;
            transition: transform 0.3s;
        }

        .btn-yes, .btn-continue {
            background-color: #ff4d6d;
            color: white;
            box-shadow: 0 4px 10px rgba(255, 77, 109, 0.4);
            z-index: 10;
        }

        .btn-no {
            background-color: #e0e0e0;
            color: #555;
            position: absolute; 
            left: 55%; 
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
            color: #ff4d6d;
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
        <div class="card" id="card1">
            <img src="9e034dd866d22d2ca42360b4d82f2bc7.jpg" alt="صورة لطيفة" class="main-image">
            <h1>إلى زوزايتي الغالية 💖</h1>
            <p>أريد أرسلج رسالة من قلبي بيها كل المشاعر اللي ما كدرت أحجيها. رسالة تخبرج شكد أنتي مهمة بحياتي.</p>
            <p style="font-weight: bold;">مستعدة تكملين وتعرفين كل الكلام؟</p>

            <div class="buttons-container">
                <button class="btn-continue" onclick="continueToLove()">أكيد أستمر 🌹</button>
                <button class="btn-no" id="noBtn1" onmouseover="moveButton('noBtn1')" ontouchstart="moveButton('noBtn1')" onclick="moveButton('noBtn1')">لا ما ماريد ولي متحرش 😒</button>
            </div>
        </div>

        <div class="hidden-content" id="restOfMessage">

            <div class="card">
                <h1>ضحكتج وعيونج ✨</h1>
                <p>ضحكتج صارت هي الأغنية المفضلة عندي، وعيونج هي العالم اللي أضيع بي وألكَى نفسي بي بنفس الوقت. أنتي النعمة اللي أدعي ربي يحفظها إلي.</p>
            </div>

            <div class="card">
                <h1>أمان وراحة 🫂</h1>
                <p>وياج أحس بالأمان، أحس إني أكدر أكون على طبيعتي بدون خوف. كل كلمة حلوة منج تنطيني طاقة، وأنتي صرتي جزء مني ومن روحي.</p>
            </div>

            <div class="card">
                <h1>كلام القلب ❤️</h1>
                <p>كنت خايف أحجي، بس خوفي من إني أخسرج أكبر من خوفي من الاعتراف. قلبي ملى من الحب وما عاد يكدر يسكت أكثر من هيج، لازم تعرفين شعوري.</p>
            </div>

            <div class="card" id="card5">
                <h1>والسؤال هو... أحبج يا أغلى شي</h1>
                <p>أريد أكلج شي بقلبي من زمان..</p>
                
                <div class="poem">
                    "يا أجمل الصدف يا أحلى أقداري<br>
                    حبج سكن بالروح وغير أفكاري<br>
                    أنتِ النبض للقلب وأنتِ الهوا للصدار<br>
                    فدوا أروحلج يا زوزايتي يا نوري ونهاري"
                </div>

                <p style="margin-top: 15px; font-weight: bold;">تقبلين تكملين حياتج وياي؟ وتصيرين حبيبتي؟</p>

                <div class="buttons-container">
                    <button class="btn-yes" onclick="showLove()">أكيد اقبل احبك حموداتيي❤️</button>
                    <button class="btn-no" id="noBtn2" onmouseover="moveButton('noBtn2')" ontouchstart="moveButton('noBtn2')" onclick="moveButton('noBtn2')">لا ما أريد 😒</button>
                </div>
            </div>
        </div> </div>

    <div id="success-message">
        <div class="floating-hearts">❤️❤️❤️</div>
        <br>
        <h2> ❤️واني هم احبج و اموت عليج</h2>
        <p>أسعد إنسان بالدنيا آني اليوم</p>
        <p>أحبج زوزايتي</p>
        <div class="floating-hearts">❤️❤️❤️</div>
    </div>

    <script>
        // دالة تحريك الزر "لا"
        function moveButton(btnId) {
            var btnNo = document.getElementById(btnId);
            
            // تحريك عشوائي في نطاق صغير لجعل الزر يهرب
            var randomX = Math.floor(Math.random() * 200) - 100; // بين -100 و +100
            var randomY = Math.floor(Math.random() * 80) - 40;   // بين -40 و +40
            
            // تطبيق الموقع الجديد
            btnNo.style.transform = `translate(${randomX}px, ${randomY}px)`;
        }

        // دالة الضغط على "استمرار"
        function continueToLove() {
            var rest = document.getElementById('restOfMessage');
            var card1 = document.getElementById('card1');

            // إظهار المحتوى المخفي
            rest.classList.add('show-content');
            
            // إخفاء الأزرار التفاعلية من البطاقة الأولى بعد الاستمرار
            card1.querySelector('.buttons-container').style.display = 'none';
            
            // التمرير إلى الفقرة الثانية (بداية المحتوى الجديد)
            rest.scrollIntoView({ behavior: 'smooth' });
        }

        // دالة الضغط على "نعم" النهائي
        function showLove() {
            document.getElementById('success-message').style.display = 'flex';
            document.body.style.overflow = 'hidden'; 
        }
    </script>
</body>
</html>
