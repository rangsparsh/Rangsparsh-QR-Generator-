
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rangsparsh Printers - QR Generator</title>
    
    <!-- Adsterra Head Ad (इसे Adsterra डैशबोर्ड से अपना कोड रिप्लेस करें) -->
    <script src="//www.profitabledisplaynetwork.com/your-header-ad-code.js"></script>
    
    <!-- CSS स्टाइल -->
    <style>
        * {
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        body {
            background: #f0f2f5;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #2c3e50;
            text-align: center;
        }
        .input-group {
            margin: 20px 0;
            text-align: center;
        }
        input {
            width: 80%;
            padding: 12px;
            border: 2px solid #3498db;
            border-radius: 5px;
            font-size: 16px;
        }
        button {
            background: #3498db;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px;
        }
        button:hover {
            background: #2980b9;
        }
        #qrcode {
            text-align: center;
            margin: 20px 0;
        }
        .ads {
            text-align: center;
            margin: 20px 0;
        }
        footer {
            text-align: center;
            margin-top: 30px;
            color: #7f8c8d;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>रंगस्पर्श प्रिंटर्स QR जनरेटर</h1>
        
        <!-- Adsterra Banner Ad (यहाँ अपना बैनर कोड पेस्ट करें) -->
        <div class="ads">
            <script src="//www.profitabledisplaynetwork.com/your-banner-ad-code.js"></script>
        </div>

        <div class="input-group">
            <input type="text" id="qr-input" placeholder="यहाँ टेक्स्ट या URL डालें...">
            <button onclick="generateQR()">QR बनाएं</button>
            <button onclick="downloadQR()">डाउनलोड करें</button>
        </div>

        <div id="qrcode"></div>

        <!-- Adsterra Popunder Ad (Body के अंत में कोड पेस्ट करें) -->
        <script src="//www.profitabledisplaynetwork.com/your-popunder-ad-code.js"></script>
    </div>

    <footer>
        <p>© 2024 रंगस्पर्श प्रिंटर्स. सर्वाधिकार सुरक्षित.</p>
    </footer>

    <!-- QR Code Library -->
    <script src="https://cdn.jsdelivr.net/npm/qrcodejs@1.0.0/qrcode.min.js"></script>
    
    <!-- JavaScript कोड -->
    <script>
        // QR जनरेट करें
        function generateQR() {
            const text = document.getElementById('qr-input').value;
            const qrDiv = document.getElementById('qrcode');
            qrDiv.innerHTML = '';
            new QRCode(qrDiv, {
                text: text,
                width: 200,
                height: 200,
                colorDark: "#2c3e50",
                colorLight: "#ffffff"
            });
        }

        // QR डाउनलोड करें
        function downloadQR() {
            const canvas = document.querySelector("#qrcode canvas");
            if (canvas) {
                const link = document.createElement('a');
                link.download = 'Rangsparsh-QR.png';
                link.href = canvas.toDataURL();
                link.click();
            } else {
                alert('पहले QR जनरेट करें!');
            }
        }
    </script>
</body>
</html>
