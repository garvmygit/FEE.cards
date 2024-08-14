<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Card Page</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #000000;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        
        .container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            padding: 20px;
            max-width: 1200px;
        }
        
        .card {
            position: relative;
            background-color: #ffffff;
            border-radius: 15px;
            padding: 30px;
            border: 20px ;
            text-align: center;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.08);
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 18px;
            font-weight: bold;
            color: #333;
            overflow: hidden;
        }
        
        .card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border-radius: 15px;
            z-index: -1;
            transition: opacity 0.3s ease;
            opacity: 0;
        }
        
        .card:hover::before {
            opacity: 1;
        }
        
        .card:hover {
            box-shadow: 0 15px 25px rgba(0, 0, 0, 0.15);
          
        }
        
        .card:active {
            transform: translateY(0);
        }
        
        @media (max-width: 768px) {
            .container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 480px) {
            .container {
                grid-template-columns: 1fr;
            }
        }
        
    </style>
</head>
<body>
    <div class="container">
        <div class="card" onclick="redirectToPage(1)">Card 1</div>
        <div class="card" onclick="redirectToPage(2)">Card 2</div>
        <div class="card" onclick="redirectToPage(3)">Card 3</div>
        <div class="card" onclick="redirectToPage(4)">Card 4</div>
        <div class="card" onclick="redirectToPage(5)">Card 5</div>
        <div class="card" onclick="redirectToPage(6)">Card 6</div>
        <div class="card" onclick="redirectToPage(7)">Card 7</div>
        <div class="card" onclick="redirectToPage(8)">Card 8</div>
        <div class="card" onclick="redirectToPage(9)">Card 9</div>
        <div class="card" onclick="redirectToPage(10)">Card 10</div>
        <div class="card" onclick="redirectToPage(11)">Card 11</div>
        <div class="card" onclick="redirectToPage(12)">Card 12</div>
    </div>

    <script >function redirectToPage(cardNumber) {
       
        const urls = {
            1: "https://www.codingninjas.com/",
            2: "https://www.codingninjas.com/",
            3: "https://www.callofduty.com/hub",
            4: "https://www.callofduty.com/hub",
            5: "https://www.geeg.it/en/home-ing/",
            6: "https://www.geeg.it/en/home-ing/",
            7: "https://www.geeg.it/en/home-ing/",
            8: "https://www.geeg.it/en/home-ing/",
            9: "https://www.geeg.it/en/home-ing/",
            10: "https://en.wikipedia.org/wiki/Wiki",
            11: "https://en.wikipedia.org/wiki/Wiki",
            12: "https://en.wikipedia.org/wiki/Wiki"
        };
    
     
        if (urls[cardNumber]) {
            window.location.href = urls[cardNumber];
        }
    }
    </script>
</body>
</html>
