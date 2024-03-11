<!DOCTYPE html>
<html>
<head>
    <style>
        .container {
            display: flex;
            justify-content: flex-start;
            align-items: center;
            padding: 20px;
        }

        .painting-frame {
            cursor: pointer;
            width: 300px;
            height: 400px;
            margin-right: 40px; /* Added margin for spacing */
        }

        .painting-info {
            width: 300px;
            height: 400px;
            background-color: #f0f0f0;
            display: none;
            padding: 20px;
        }

        .container:hover .painting-info,
        .painting-frame.clicked + .painting-info {
            display: block;
        }
    </style>
</head>
<body>
    <div class="container">
        <img class="painting-frame" src="mona_lisa.jpg" alt="Mona Lisa" onclick="toggleInfo()">
        <div class="painting-info">
            <h2>Title of Painting</h2>
            <p>Description of the painting goes here.</p>
            <p>Artist: Leonardo da Vinci</p>
            <p>Year: 1503–1506</p>
        </div>
    </div>

    <!-- Add more paintings as needed -->

    <script>
        function toggleInfo() {
            var info = document.querySelector('.painting-frame');
            info.classList.toggle("clicked");
        }
    </script>
</body>
</html>
