# Ex.08 Design of Interactive Image Gallery
# Date:9/5/2025
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Top Anime Characters</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
      color: #fff;
      animation: backgroundShift 10s infinite alternate;
    }

    @keyframes backgroundShift {
      0% { background-position: 0% 50%; }
      100% { background-position: 100% 50%; }
    }

    h1 {
      text-align: center;
      font-size: 3rem;
      margin: 40px 0 20px;
      background: linear-gradient(to right, #ff512f, #dd2476);
      -webkit-background-clip: text;
      color: transparent;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
      padding: 30px;
      max-width: 1400px;
      margin: auto;
    }

    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 16px;
      cursor: pointer;
      box-shadow: 0 10px 25px rgba(255, 0, 140, 0.4);
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }

    .gallery-item:hover {
      transform: scale(1.05);
      box-shadow: 0 20px 40px rgba(255, 0, 140, 0.6);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.15);
    }

    .caption {
      position: absolute;
      bottom: 0;
      background: rgba(0, 0, 0, 0.7);
      width: 100%;
      padding: 12px;
      text-align: center;
      font-size: 16px;
      color: #ff9ee6;
      font-weight: bold;
      letter-spacing: 1px;
    }

    .modal {
      display: none;
      position: fixed;
      inset: 0;
      background-color: rgba(0, 0, 0, 0.95);
      justify-content: center;
      align-items: center;
      z-index: 999;
    }

    .modal img {
      max-width: 90%;
      max-height: 90%;
      border: 4px solid #ff3cac;
      border-radius: 12px;
      box-shadow: 0 0 30px #ff3cac;
    }

    .modal .close {
      position: absolute;
      top: 25px;
      right: 35px;
      font-size: 40px;
      color: #fff;
      cursor: pointer;
      text-shadow: 0 0 10px #ff3cac;
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 14px;
      color: #aaa;
      background-color: #1a1a1a;
      border-top: 1px solid #333;
    }
  </style>
</head>
<body>

  <h1>🔥 Top Anime Characters</h1>

  <div class="gallery">
    <div class="gallery-item" onclick="openModal('GOKU.jpg')">
      <img src="GOKU.jpg" alt="Goku">
      <div class="caption">Goku - Dragon Ball Z</div>
    </div>
    <div class="gallery-item" onclick="openModal('LUFFY.jpg')">
      <img src="LUFFY.jpg" alt="Luffy">
      <div class="caption">Monkey D. Luffy - One Piece</div>
    </div>
    <div class="gallery-item" onclick="openModal('NARUTO.jpg')">
      <img src="NARUTO.jpg" alt="Naruto">
      <div class="caption">Naruto Uzumaki - Naruto</div>
    </div>
    <div class="gallery-item" onclick="openModal('EREN.jpg')">
      <img src="EREN.jpg" alt="Eren Yeager">
      <div class="caption">Eren Yeager - Attack on Titan</div>
    </div>
    <div class="gallery-item" onclick="openModal('TANJIRO.jpg')">
      <img src="TANJIRO.jpg" alt="Tanjiro Kamado">
      <div class="caption">Tanjiro Kamado - Demon Slayer</div>
    </div>
  </div>

  <!-- Modal -->
  <div class="modal" id="imageModal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img id="modalImage" src="" alt="">
  </div>

  <footer>
    &copy; 2025 designed by HARI KRISHNAN [24006166]. All Rights Reserved.
  </footer>

  <script>
    function openModal(src) {
      const modal = document.getElementById('imageModal');
      const modalImg = document.getElementById('modalImage');
      modalImg.src = src;
      modal.style.display = 'flex';
    }

    function closeModal() {
      const modal = document.getElementById('imageModal');
      modal.style.display = 'none';
    }
  </script>
</body>
</html>
```
# OUTPUT:

![alt text](<Screenshot 2025-05-09 213824.png>)

![alt text](<Screenshot 2025-05-09 213838.png>)

![alt text](<Screenshot 2025-05-09 213852.png>)

![alt text](<Screenshot 2025-05-09 213904.png>)

![alt text](<Screenshot 2025-05-09 213917.png>)

![alt text](<Screenshot 2025-05-09 213929.png>)


# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
