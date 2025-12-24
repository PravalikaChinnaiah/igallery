# Ex.07 Design of Interactive Image Gallery
## Date:23.12.2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:

```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title> 
</head>  
<body> 
<div class="gallery-container"> 
<img id="galleryImage" class="gallery-image" src="sundar.jpg" height="40%" width="40%"> 
<div id="caption" class="caption">Caption for Image 1</div> 
<div class="gallery-buttons"> 
<button onclick="prevImage()">Previous</button> 
<button onclick="nextImage()">Next</button> 
</div> 
</div> 
<script> 
const images = [ 
{ src: "rollsroyce.jpg", caption: "Caption for Image 1" }, 
{ src: "lamborghini.jpg", caption: "Caption for Image 2" }, 
{ src: "ferrari 1.jpg", caption: "Caption for Image 3" } 
]; 
let currentIndex = 0; 
function updateGallery( )  
{ 
document.getElementById("galleryImage").src = images[currentIndex].src; 
document.getElementById("caption").textContent = images[currentIndex].caption; 
} 
function nextImage( )  
{ 
currentIndex = (currentIndex + 1) % images.length; 
updateGallery( ); 
} 
function prevImage( )  
{ 
currentIndex = (currentIndex - 1 + images.length) % images.length; 
updateGallery( ); 
} 
</script> 
</body>
</html>

.gallery-container  
{ 
            position: relative; 
            max-width: 600px; 
            margin: auto; 
            background: white; 
            padding: 10px; 
            border-radius: 10px; 
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); 
         } 
         .gallery-image  
{ 
            width: 500%; 
            height: 600px; 
            object-fit: cover; 
            border-radius: 10px; 
         } 
         .caption  
{ 
            margin-top: 10px; 
            font-size: 18px; 
         } 
         .gallery-buttons  
{ 
            display: flex; 
            justify-content: space-between; 
            margin-top: 15px; 
         } 
         button  
{ 
            padding: 10px 20px; 
            cursor: pointer; 
            border: none; 
            border-radius: 5px; 
            background-color: #007BFF; 
            color: white; 
            transition: 0.3s; 
         } 

         ```

## OUTPUT:
Screenshot 2025-12-24 100514.png
Screenshot 2025-12-24 100525.png
Screenshot 2025-12-24 100539.png



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
