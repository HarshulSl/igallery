# Ex.08 Design of Interactive Image Gallery
## Date:17/12/24

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
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Celebrity Gallery</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background-color: #2e2e2e;
            color: #f4f4f9;
            line-height: 1.6;
        }

        header {
            background: #1a1a1a;
            color: #f4f4f9;
            text-align: center;
            padding: 2rem 1rem;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            color: #ff6347;
        }

        header p {
            font-size: 1.2rem;
        }

        main {
            padding: 2rem;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease-in-out;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-item::before {
            content: '';
            display: block;
            padding-top: 100%;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            top: 0;
            left: 0;
            cursor: pointer;
        }

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease-in-out;
        }

        .overlay p {
            font-size: 1.5rem;
            font-weight: bold;
        }

        .gallery-item:hover .overlay {
            opacity: 1;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .modal-content {
            max-width: 90%;
            max-height: 90%;
            margin: auto;
        }

        .modal img {
            width: 100%;
            height: auto;
        }

        .close {
            position: absolute;
            top: 10px;
            right: 10px;
            color: #f4f4f9;
            font-size: 2rem;
            cursor: pointer;
            background: rgba(0, 0, 0, 0.7);
            border: none;
            padding: 10px;
            border-radius: 50%;
        }

        footer {
            text-align: center;
            padding: 1.5rem 0;
            background: #1a1a1a;
            color: #f4f4f9;
            margin-top: 2rem;
        }

        footer p {
            font-size: 1rem;
        }

        .footer-credits {
            font-size: 0.9rem;
            color: #ff6347;
        }
    </style>
</head>
<body>
    <header>
        <h1>Celebrity Interactive Gallery</h1>
        <p>Explore our curated collection of famous celebrities</p>
    </header>
    <main>
        <section class="gallery">
            <div class="gallery-item">
                <img src="cel1.jpg" alt="Chris Hemsworth" onclick="openModal(this)">
                <div class="overlay"><p>Chris Hemsworth</p></div>
            </div>
            <div class="gallery-item">
                <img src="cel2.jpg" alt="Leonardo DiCaprio" onclick="openModal(this)">
                <div class="overlay"><p>Leonardo DiCaprio</p></div>
            </div>
            <div class="gallery-item">
                <img src="cel3.jpg" alt="Ryan Gosling" onclick="openModal(this)">
                <div class="overlay"><p>Ryan Gosling</p></div>
            </div>
            <div class="gallery-item">
                <img src="cel4.jpg" alt="Will Smith" onclick="openModal(this)">
                <div class="overlay"><p>Will Smith</p></div>
            </div>
            <div class="gallery-item">
                <img src="cel5.jpg" alt="Robert Downey Jr." onclick="openModal(this)">
                <div class="overlay"><p>Robert Downey Jr.</p></div>
            </div>
        </section>
    </main>

    <div class="modal" id="myModal">
        <span class="close" onclick="closeModal()">&times;</span>
        <div class="modal-content">
            <img id="modal-img" src="" alt="Full Image">
        </div>
    </div>

    <footer>
        <p>&copy; 2024 Celebrity Gallery. All Rights Reserved.</p>
        <p class="footer-credits">Designed and Developed by HARSHUL SL</p>
    </footer>

    <script>
        function openModal(img) {
            var modal = document.getElementById("myModal");
            var modalImg = document.getElementById("modal-img");
            modal.style.display = "flex";
            modalImg.src = img.src;
        }

        function closeModal() {
            var modal = document.getElementById("myModal");
            modal.style.display = "none";
        }

        window.onclick = function(event) {
            var modal = document.getElementById("myModal");
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
    </script>
</body>
</html>


```

## OUTPUT:
![alt text](image.png)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
