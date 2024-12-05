<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فرم ثبت‌نام</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .form-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }

        h2 {
            text-align: center;
            color: #333;
        }

        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
        }

        input[type="text"],
        input[type="email"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            width: 100%;
            padding: 10px;
            background-color: #28a745;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>فرم ثبت‌نام</h2>
        <form id="registrationForm">
            <label for="name">نام:</label>
            <input type="text" name="name" required>
            
            <label for="email">ایمیل:</label>
            <input type="email" name="email" required>
            
            <label for="phone">شماره تماس:</label>
            <input type="text" name="phone" required>
            
            <button type="submit">ثبت‌نام</button>
        </form>
    </div>

    <script>
        document.getElementById('registrationForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const formData = new FormData(this);
            const name = formData.get('name');
            const email = formData.get('email');
            const phone = formData.get('phone');

            // شماره روبیکا خود را در اینجا وارد کنید
            const rubikaNumber = '@kali__linux__ERROR';
            const message = `ثبت‌نام جدید:\nنام: ${name}\nایمیل: ${email}\nشماره تماس: ${phone}`;
            const rubikaLink = `https://rubika.ir/send?phone=${rubikaNumber}&text=${encodeURIComponent(message)}`;

            // باز کردن لینک روبیکا
            window.open(rubikaLink, '_blank');
        });
    </script>
</body>
</html>
