# Ex.08 Design of Interactive Image Gallery
## Date:

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

<!DOCTYPE html>
<html>
<head>
  <title>Interactive Image Gallery</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Cinzel&display=swap');

    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: 'Cinzel', serif;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('bg.jpg') no-repeat center center fixed;
      background-size: cover;
      opacity: 0.6; 
      z-index: -1;
    }

    body {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }

    .mainbox {
      width: 90%;
      max-width: 900px;
      border: 2px solid #6F826A;
      overflow: hidden;
      border-radius: 15px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.5);
      position: relative;
      background: rgba(255, 255, 255, 0.85); 
    }

    .images {
      display: flex;
      width: 100%;
      transition: transform 0.5s ease-in-out;
    }

    .slide {
      min-width: 100%;
    }

    .slide img {
      width: 100%;
      height: auto;
      object-fit: contain;
      background: black;
      display: block;
    }

    .button {
      top: 50%;
      position: absolute;
      transform: translateY(-50%);
      background: rgba(255, 255, 255, 0.3);
      border: none;
      font-size: 2rem;
      color: #EDE8DC;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 50%;
      transition: background 0.3s;
      z-index: 2;
    }

    .button:hover {
      background: rgba(255, 255, 255, 0.6);
    }

    .left {
      left: 15px;
    }

    .right {
      right: 15px;
    }

    .txt-up, .text-bottom {
      width: 80%;
      max-width: 700px;
      text-align: center;
      font-family: Arial, sans-serif;
      margin: 10px 0;
    }

    .txt-up {
      font-weight: bolder;
      color: #143D60;
    }

    .txt-down {
      margin-top: 7px;
      font-weight: bold;
      line-height: 25px;
      color: #27667B;
    }

    .txt-mid {
      width: 100%;
      max-width: 900px;
      text-align: center;
      font-family: 'Cinzel', serif;
      margin: 10px 0;
      font-size: 58px;
      font-weight: super bold;
      background: linear-gradient(90deg, #280736, #4b215e, #3c1c9d);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      color: transparent;
      user-select: none;
    }
  </style>
</head>
<body>
  <div class="txt-up"><h1>Interactive Image Gallery</h1></div>
  
  <div class="mainbox">
    <div class="images" id="images">
      <div class="slide"><img src="1.img.jpg" alt="img1"></div>
      <div class="slide"><img src="2.img.jpg" alt="img2"></div>
      <div class="slide"><img src="3.img.jpg" alt="img3"></div>
      <div class="slide"><img src="4.ing.jpg" alt="img4"></div>
      <div class="slide"><img src="5.img.jpg" alt="img5"></div>
      
    </div>
    <button class="button left" id="left">&lt;</button>
    <button class="button right" id="right">&gt;</button>
  </div>

  <div class="txt-down">
    <h3>Name: SWETHA NIVASINI<br>Register No: 212224040345</h3>
  </div>

  <script>
    const slider = document.getElementById('images');
    const slides = document.querySelectorAll('.slide');
    const left_bt = document.getElementById('left');
    const right_bt = document.getElementById('right');
    let currentIndex = 0;

    function updateSlider() {
      slider.style.transform = `translateX(-${currentIndex * 100}%)`;
    }

    function nextSlide() {
      currentIndex = (currentIndex + 1) % slides.length;
      updateSlider();
    }

    function prevSlide() {
      currentIndex = (currentIndex - 1 + slides.length) % slides.length;
      updateSlider();
    }

    right_bt.addEventListener('click', nextSlide);
    left_bt.addEventListener('click', prevSlide);
  </script>
</body>
</html>







## OUTPUT:



![Screenshot 2025-05-27 205622](https://github.com/user-attachments/assets/6789889f-e9d7-410b-9abc-e2db9bb969dd)



![Screenshot 2025-05-27 205642](https://github.com/user-attachments/assets/8765ddf2-c0fc-414d-8402-2b53dcd3273a)



![Screenshot 2025-05-27 205656](https://github.com/user-attachments/assets/0b7747fe-5237-49d3-bb32-adf34c99c998)



![Screenshot 2025-05-27 205709](https://github.com/user-attachments/assets/423ec131-45d0-4927-b773-91843d99d293)



![Screenshot 2025-05-27 205717](https://github.com/user-attachments/assets/8f7af1a1-b461-4770-b059-cbd72d11b628)










## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
