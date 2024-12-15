// Array of image URLs (replace these with your image paths)
const images = [
    'image1.jpg', 'image2.jpg', 'image3.jpg', 
    'image4.jpg', 'image5.jpg', 'image6.jpg', 
    'image7.jpg', 'image8.jpg', 'image9.jpg'
];

// URL for the static GIF
const staticGif = 'https://upload.wikimedia.org/wikipedia/commons/d/d2/Static.gif';

// Reference to the HTML image element
const imageContainer = document.getElementById('image-container');

// Function to show an image
function showImage(imageUrl) {
    imageContainer.src = imageUrl;
}

// Function to rotate through images
async function rotateImages() {
    while (true) {
        for (let i = 0; i < images.length; i++) {
            // Show static GIF
            showImage(staticGif);
            await new Promise(resolve => setTimeout(resolve, 1000)); // Show static for 1 second

            // Show the next image
            showImage(images[i]);
            const randomInterval = Math.random() * 3000 + 3000; // Random interval between 3-6 seconds
            await new Promise(resolve => setTimeout(resolve, randomInterval));

            // Move the image to the back of the array
            const shiftedImage = images.shift();
            images.push(shiftedImage);
        }
    }
}

// Start the rotation
rotateImages();
