COMPANY NAME- DYNAMITE WEBTECH

NAME- ODDINA KAVYA

INTERN ID: u75da

CODE FOR TASK 3: IMAGE SLIDER

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Image Slider</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #222;
    }

    .slider {
      position: relative;
      max-width: 800px;
      margin: 50px auto;
      overflow: hidden;
      border-radius: 15px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.3);
    }

    .slides {
      display: flex;
      transition: transform 0.5s ease-in-out;
      width: 100%;
    }

    .slide {
      min-width: 100%;
      transition: opacity 0.5s ease;
    }

    .slide img {
      width: 100%;
      display: block;
    }

    .arrow {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      font-size: 2rem;
      color: white;
      background: rgba(0, 0, 0, 0.5);
      padding: 10px;
      cursor: pointer;
      z-index: 2;
      user-select: none;
      border-radius: 50%;
    }

    .arrow:hover {
      background: rgba(0, 0, 0, 0.8);
    }

    .arrow-left {
      left: 10px;
    }

    .arrow-right {
      right: 10px;
    }
  </style>
</head>
<body>
  <div class="slider">
    <div class="arrow arrow-left" onclick="prevSlide()">&#10094;</div>
    <div class="arrow arrow-right" onclick="nextSlide()">&#10095;</div>
    <div class="slides" id="slides">
      <div class="slide"><img src="e:\image1.jpg" alt="1"></div>
      <div class="slide"><img src="e:\image2.jpg" alt="2"></div>
      <div class="slide"><img src="e:\image3.png" alt="3"></div>
    </div>
  </div>

  <script>
    let currentIndex = 0;
    const slides = document.getElementById('slides');
    const totalSlides = slides.children.length;

    function updateSlide() {
      slides.style.transform = `translateX(-${currentIndex * 100}%)`;
    }

    function nextSlide() {
      currentIndex = (currentIndex + 1) % totalSlides;
      updateSlide();
    }

    function prevSlide() {
      currentIndex = (currentIndex - 1 + totalSlides) % totalSlides;
      updateSlide();
    }

    // Auto-slide every 4 seconds
    setInterval(() => {
      nextSlide();
    }, 4000);
  </script>
</body>
</html>

output for task 3 :image_slider

![Image](https://github.com/user-attachments/assets/b44d0501-d65b-40cc-8ef2-220e7dc9bb6b)

![Image](https://github.com/user-attachments/assets/05450b7b-8616-4ffe-86ca-15b8963432b0)

![Image](https://github.com/user-attachments/assets/19f558d8-20fe-4799-97c5-a2b76026e6e8)


