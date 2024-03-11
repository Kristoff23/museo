HI
<html>
<head>
    <style>
        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            margin-right: 10cm; /* Adjust the distance between images */
        }

        .painting-frame {
            cursor: pointer;
            width: 300px;
            height: 400px;
        }

        .painting-info {
            display: none;
            position: relative;
            padding: 20px;
            animation: slideIn 0.5s forwards;
            width: 300px;
            height: 400px;
            background-image: url('painting_info_bg.jpg');
            background-size: cover;
            color: #fff;
            opacity: 0.9;
        }

        .arrow-button {
            display: none;
            position: absolute;
            top: 50%;
            left: -40px;
            transform: translateY(-50%);
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
            font-size: 18px;
            border-radius: 50%;
            width: 40px;
            height: 40px;
        }

        .arrow-button::after {
            content: '';
            position: absolute;
            width: 0;
            height: 0;
            border-top: 8px solid transparent;
            border-bottom: 8px solid transparent;
            border-right: 12px solid #fff;
            left: 50%;
            top: 50%;
            transform: translateY(-50%) translateX(-50%);
        }

        .painting-frame:hover + .painting-info,
        .painting-info.active {
            display: block;
        }

        .arrow-button.active {
            display: block;
        }

        @keyframes slideIn {
            from {
                transform: translateX(100%);
            }
            to {
                transform: translateX(0);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <img class="painting-frame" src="Jose Rizal.jpg" alt="Jose Rizal">
          background-attachment: fixed;
        <div class="painting-info">
            <h2>Title of Painting</h2>
            <p>Description of the painting goes here.</p>
            <p>Artist: Leonardo da Vinci</p>
            <p>Year: 1503–1506</p>
            <button class="arrow-button"></button>
        </div>
    </div>

    <!-- Add more paintings as needed -->

    <script>
        document.querySelectorAll('.painting-frame').forEach(paintingFrame => {
            const paintingInfo = paintingFrame.nextElementSibling;
            const arrowButton = paintingInfo.querySelector('.arrow-button');

            paintingFrame.addEventListener('click', () => {
                paintingInfo.classList.toggle('active');
                arrowButton.classList.toggle('active');
            });

            arrowButton.addEventListener('click', () => {
                paintingInfo.classList.toggle('active');
                arrowButton.classList.toggle('active');
            });
        });
    </script>
</body>
</html>
