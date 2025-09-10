<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حساب المعدلات الدراسية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c 0%, #2a4b8c 50%, #3a6ccc 100%);
            color: #fff;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            text-align: center;
            background-attachment: fixed;
            background-size: cover;
        }
        
        .header {
            margin-bottom: 30px;
        }
        
        .logo {
            width: 120px;
            height: 120px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            border: 3px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .logo i {
            font-size: 50px;
            color: #fff;
        }
        
        .container {
            max-width: 1000px;
            width: 100%;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(12px);
            border-radius: 25px;
            padding: 40px 30px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
            border: 1px solid rgba(255, 255, 255, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .container::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            transform: rotate(30deg);
            pointer-events: none;
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 25px;
            color: #fff;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3);
            position: relative;
            padding-bottom: 15px;
        }
        
        h1::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 30%;
            right: 30%;
            height: 3px;
            background: linear-gradient(90deg, transparent, #ffffff, transparent);
            border-radius: 3px;
        }
        
        p {
            font-size: 1.25rem;
            line-height: 1.7;
            margin-bottom: 35px;
            color: #f0f0f0;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
        }
        
        .buttons-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 25px;
            margin-top: 40px;
        }
        
        .btn {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            width: 300px;
            height: 200px;
            background: rgba(255, 255, 255, 0.15);
            border-radius: 18px;
            padding: 25px;
            text-decoration: none;
            color: #fff;
            transition: all 0.4s ease;
            border: 1px solid rgba(255, 255, 255, 0.25);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
            position: relative;
            overflow: hidden;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
            transform: translateX(-100%);
            transition: transform 0.6s ease;
        }
        
        .btn:hover {
            transform: translateY(-8px) scale(1.03);
            background: rgba(255, 255, 255, 0.25);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.25);
        }
        
        .btn:hover::before {
            transform: translateX(100%);
        }
        
        .btn i {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease;
        }
        
        .btn:hover i {
            transform: scale(1.1);
        }
        
        .btn h3 {
            font-size: 1.5rem;
            margin-bottom: 12px;
            font-weight: 600;
        }
        
        .btn p {
            font-size: 1rem;
            margin: 0;
            color: #e0e0e0;
        }
        
        .features {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin: 40px 0;
        }
        
        .feature {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 15px;
            width: 160px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.15);
        }
        
        .feature i {
            font-size: 2rem;
            margin-bottom: 10px;
            color: #aaccff;
        }
        
        .footer {
            margin-top: 50px;
            color: rgba(255, 255, 255, 0.8);
            font-size: 1rem;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
        }
        
        @media (max-width: 768px) {
            .buttons-container {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 350px;
                height: 180px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            p {
                font-size: 1.1rem;
            }
            
            .features {
                gap: 15px;
            }
            
            .feature {
                width: 140px;
                padding: 12px;
            }
            
            .feature i {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <div class="logo">
            <i class="fas fa-calculator"></i>
        </div>
        <h1>حساب علامات امتحان الإجازة لطلاب الطب </h1>
    </div>
    
    <div class="container">
        <p>هذا الموقع يوفر لك أدوات متقدمة لحساب حد النجاح في كل مادة ومعدل امتحان الإجازة الإجمالي بسهولة وسرعة. اختر الأداة التي تناسب احتياجاتك من الخيارات أدناه.</p>
        
        </div>
        
        <div class="buttons-container">
            <a href="https://webdr-creator.github.io/Cal/Exam.html" class="btn">
                <i class="fas fa-file-alt"></i>
                <h3>حساب حد النجاح</h3>
                <p>أداة لحساب عدد الأسئلة اللازمة للنجاح</p>
            </a>
            
            <a href="https://webdr-creator.github.io/Cal/Exam.html" class="btn">
                <i class="fas fa-chart-bar"></i>
                <h3>حساب معدل الامتحان</h3>
                <p>أداة  لحساب معدل الامتحان الاجمالي </p>
            </a>
        </div>
    </div>
    
    <div class="footer">
        <p>جميع الحقوق محفوظة © 2023</p>
    </div>

    <script>
        // تأثيرات تفاعلية بسيطة
        document.addEventListener('DOMContentLoaded', function() {
            const buttons = document.querySelectorAll('.btn');
            
            buttons.forEach(button => {
                button.addEventListener('mouseenter', function() {
                    this.querySelector('i').style.transform = 'scale(1.2) rotate(5deg)';
                });
                
                button.addEventListener('mouseleave', function() {
                    this.querySelector('i').style.transform = 'scale(1)';
                });
            });
            
            // تأثير الكتابة للنص الرئيسي
            const title = document.querySelector('h1');
            const originalText = title.textContent;
            title.textContent = '';
            let i = 0;
            
            function typeWriter() {
                if (i < originalText.length) {
                    title.textContent += originalText.charAt(i);
                    i++;
                    setTimeout(typeWriter, 100);
                }
            }
            
            setTimeout(typeWriter, 500);
        });
    </script>
</body>
</html>
