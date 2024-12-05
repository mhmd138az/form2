<h1>سفارش شما </h1>
<h1>از طریق واتساپ ثبت میگردد </h1>
<h1>!پس لطفا وی پی ان خود را روشن کنید</h1>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فرم ثبت سفارش</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #eaefd8;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        h1{
           text-align: center;
        }
        .form-container {
            background-color: #ffffff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            width: 400px;
            transition: transform 0.3s;
        }
        .form-container:hover {
            transform: scale(1.02);
        }
        h2 {
            text-align: center;
            color: #333;
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
        }
        input[type="text"],
        input[type="email"],
        input[type="number"]
        input[type="time"] {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #1c69b6;
            border-radius: 5px;
            font-size: 16px;
        }
        button {
            width: 100%;
            padding: 12px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 18px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #0056b3;
        }
        .footer {
            text-align: center;
            margin-top: 15px;
            font-size: 14px;
            color: #777;
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>فرم ثبت سفارش</h2>
        <form id="orderForm">
            <label for="name">نام:</label>
            <input type="text" name="name" required>
            <label for="email">چی میخوای؟:</label>
            <input type="text" name="email" required>
            <label for="phone">شماره تماس:</label>
            <input type="text" name="phone" required>
            <label for="order">تعداد:</label>
            <input type="text" name="order" required>
             <label for="time">زمان تحویل سفارش:</label>
            <input type="text" name="time" required>
            <button type="submit">ثبت سفارش</button>
        </form>
        <div class="footer">با تشکر از شما!</div>
    </div>
    <script>
        document.getElementById('orderForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const formData = new FormData(this);
            const name = formData.get('name');
            const email = formData.get('email');
            const phone = formData.get('phone');
            const order = formData.get('order');
            const order = formData.get('time');
            // شماره واتساپ خود را در اینجا وارد کنید
            const whatsappNumber = '+989178537782';
            const message = `ثبت سفارش جدید:\nنام: ${name}\nنام محصول: ${email}\nشماره تماس: ${phone}\nتعداد: ${order}\nزمان تحویل سفارش؟ ${time}`;
            const whatsappLink = `https://api.whatsapp.com/send?phone=${whatsappNumber}&text=${encodeURIComponent(message)}`;
            // باز کردن لینک واتساپ
            window.open(whatsappLink, '_blank');
        });
    </script>
</body>
</html>
