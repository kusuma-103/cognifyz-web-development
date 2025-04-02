<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Manipulation</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            background: radial-gradient(circle, #ff99c2, #ffcc80, #c2e9fb); /* Radiant radial gradient */
            background-size: 200% 200%;
            animation: radiantAnimation 10s ease infinite;
        }

        @keyframes radiantAnimation {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        .slideshow-container {
            max-width: 600px;
            position: relative;
            margin: 20px auto;
            overflow: hidden;
            border-radius: 15px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
            background-color: rgba(255, 255, 255, 0.85); /* Slightly less transparent */
            padding: 25px;
        }

        .slideshow-container img {
            width: 100%;
            display: none;
            transition: opacity 0.6s ease-in-out;
        }

        .slideshow-container img.active {
            display: block;
            opacity: 1;
        }

        .slideshow-buttons {
            display: flex;
            justify-content: center;
            margin-top: 15px;
        }

        .slideshow-buttons button {
            padding: 12px 18px;
            margin: 0 8px;
            cursor: pointer;
            border: none;
            background: linear-gradient(to right, #6a11cb, #2575fc); /* Radiant button gradient */
            color: white;
            border-radius: 10px;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .slideshow-buttons button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        }

        .slide-indicators {
            display: flex;
            justify-content: center;
            margin-top: 15px;
        }

        .slide-indicators span {
            width: 14px;
            height: 14px;
            border-radius: 50%;
            background-color: #ddd;
            margin: 0 7px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .slide-indicators span.active {
            background: linear-gradient(to right, #ff8a00, #e52e71); /* Radiant dot gradient */
        }
    </style>
</head>
<body>

    <div class="slideshow-container">
        <img class="active" src="https://i.pinimg.com/736x/90/12/24/901224c8a9bd40e42089bd0a40a014ba.jpg" alt="Radiant Slide 1">
        <img src="https://i.pinimg.com/736x/71/3a/a3/713aa35e67a53ca7c617ebcf6c7a66c7.jpg" alt="Radiant Slide 2">
        <img src="https://w0.peakpx.com/wallpaper/425/726/HD-wallpaper-aesthetic-city-night-lights-world-city-lights-thumbnail.jpg
        " alt="Radiant Slide 3">
        <img src="https://cdn.prod.website-files.com/626cc9edd198e9018a043b04/62ec62a78ee1cc43f15cf053_1466828062-a0a31957cef0712176810a66660d9f6eb4211d25a52dc6aa8bf3c745245d9b04-d.webp" alt="Radiant Slide 4">
    </div>

    <div class="slideshow-buttons">
        <button onclick="changeSlide(-1)">Previous</button>
        <button onclick="changeSlide(1)">Next</button>
    </div>

    <div class="slide-indicators">
        <span onclick="currentSlide(0)"></span>
        <span onclick="currentSlide(1)"></span>
        <span onclick="currentSlide(2)"></span>
        <span onclick="currentSlide(3)"></span>
    </div>

    <script>
        let slideIndex = 0;
        showSlides();

        function changeSlide(n) {
            slideIndex += n;
            showSlides();
        }

        function currentSlide(n) {
            slideIndex = n;
            showSlides();
        }

        function showSlides() {
            let i;
            let slides = document.querySelectorAll(".slideshow-container img");
            let dots = document.querySelectorAll(".slide-indicators span");
            if (slideIndex >= slides.length) {slideIndex = 0}
            if (slideIndex < 0) {slideIndex = slides.length - 1}
            for (i = 0; i < slides.length; i++) {
                slides[i].classList.remove("active");
                dots[i].classList.remove("active");
            }
            slides[slideIndex].classList.add("active");
            dots[slideIndex].classList.add("active");
        }

        showSlides();
    </script>
</body>
</html>
