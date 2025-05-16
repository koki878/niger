<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Image Slideshow</title>
    <style>
        body {
            background-color: #f4f4f4;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .slideshow-container {
            position: relative;
            max-width: 600px;
            margin: auto;
            padding-top: 50px;
        }
        .slide {
            display: none;
        }
        img {
            width: 100%;
            border-radius: 10px;
            border: 3px solid #ccc;
        }
        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            padding: 16px;
            color: white;
            font-size: 24px;
            background-color: rgba(0, 0, 0, 0.5);
            border: none;
            transform: translateY(-50%);
            user-select: none;
        }
        .prev { left: 0; }
        .next { right: 0; }
    </style>
</head>
<body>

<h1>Image Slideshow</h1>
<div class="slideshow-container">
    <div class="slide"><img src="dadad.jpeg" alt="Image 1"></div>
    <div class="slide"><img src="dadaddadawda.jpeg" alt="Image 2"></div>
    <div class="slide"><img src="dadadadada.jpeg" alt="Image 3"></div>
    <div class="slide"><img src="adadadada.jpeg" alt="Image 4"></div>
    <div class="slide"><img src="dadadada.jpeg" alt="Image 5"></div>
    <div class="slide"><img src="daddassadsd.jpeg" alt="Image 6"></div>

    <button class="prev" onclick="plusSlides(-1)">❮</button>
    <button class="next" onclick="plusSlides(1)">❯</button>
</div>

<script>
    let slideIndex = 0;
    showSlides();

    function showSlides() {
        let slides = document.getElementsByClassName("slide");
        for (let i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";
        }
        slideIndex++;
        if (slideIndex > slides.length) { slideIndex = 1 }
        slides[slideIndex - 1].style.display = "block";
        setTimeout(showSlides, 3000); // Change image every 3 seconds
    }

    function plusSlides(n) {
        slideIndex += n - 1;
        showSlides();
    }
</script>

</body>
</html>
