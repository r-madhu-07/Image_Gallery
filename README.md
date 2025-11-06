# Ex.08 Design of Interactive Image Gallery
# DATE: 06-11-2025
## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Image Gallery</title>
  <style>
    body {
      margin: 0;
      padding: 30px;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #46c4c8, #6C7293);
      text-align: center;
    }

    h1 {
      color: #FFF;
      margin-bottom: 20px;
      font-size: 2.5rem;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      max-width: 1200px;
      margin: auto;
    }

    .gallery img {
      width: 180px;
      height: 180px;
      object-fit: cover;
      border-radius: 50%;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }

    .gallery img:hover {
      transform: scale(1.05);
      box-shadow: 0 12px 25px rgba(0, 0, 0, 0.3);
    }

    .lightbox {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.85);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    .lightbox img {
      max-width: 90%;
      max-height: 80%;
      border-radius: 10px;
      box-shadow: 0 0 30px #000;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .footer {
      margin-top: 40px;
      color: #FFF;
      font-weight: bold;
      font-size: 1.1rem;
    }
  </style>
</head>
<body>

  <h1><i><b><u>CARTOONS IMAGE GALLERY</u> </b></i></h1><br><br>

  <div class="gallery">
    <img src="ninja.jpg" alt="pets  image 1">
    <img src="motu.jpg" alt="pets image 2">
    <img src="chotta.jpg" alt="pets image 3 ">
    <img src="shinchan.jpg" alt="pets image 4">
    <img src="tom.jpg" alt="pets Image 5">
    <img src="dora.jpg" alt="pets Image 6">
    <img src="doraemon.jpg" alt="pets Image 7">
    <img src="micky.jpg" alt="pets Image 8">
  </div>

  <div class="lightbox" id="lightbox">
    <img id="lightbox-img" src="" alt="Full View">
  </div>

  <div class="footer">
    <br><i>NAME: MADHUMITHA R<br>
 REG NO:   212224240082</i>
  </div>

  <script>
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    const galleryImgs = document.querySelectorAll('.gallery img');

    galleryImgs.forEach(img => {
      img.addEventListener('click', () => {
        lightboxImg.src = img.src;
        lightbox.style.display = 'flex';
      });
    });

    lightbox.addEventListener('click', () => {
      lightbox.style.display = 'none';
    });
  </script>

</body>
</html>
```

## OUTPUT

![alt text](<../Screenshot 2025-11-06 122238.png>)

![alt text](<../Screenshot 2025-11-06 122302.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
