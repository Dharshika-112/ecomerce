let Trolley = [];
let likedProducts = []; // Array to hold liked products

// Function to add products to the Trolley
function addToTrolley(product) {
    Trolley.push(product);
    alert(product + ' has been added to your trolley!');
    console.log('Current Trolley:', Trolley);
}

// Function to display the Trolley contents
function displayTrolley() {
    if (Trolley.length === 0) {
        alert('Your trolley is empty.');
    } else {
        alert('Your trolley contains: ' + Trolley.join(', '));
    }
}

// Function to toggle liking a product
function toggleLike(product) {
    const index = likedProducts.indexOf(product);
    if (index === -1) {
        likedProducts.push(product);
        alert(product + ' liked!');
    } else {
        likedProducts.splice(index, 1);
        alert(product + ' unliked!');
    }
    console.log('Liked Products:', likedProducts);
}

// Function to display liked products when clicking the header like button
document.querySelector('#like-header-btn').addEventListener('click', function() {
    if (likedProducts.length === 0) {
        alert('You have no liked products.');
    } else {
        alert('Liked Products: ' + likedProducts.join(', '));
    }
});

// Example function for the search bar
document.querySelector('#search-btn').addEventListener('click', function() {
    const searchTerm = document.querySelector('.search-container input').value;
    alert('Searching for: ' + searchTerm);
});

// Functionality for microphone and camera buttons
document.querySelector('#mic-btn').addEventListener('click', function() {
    alert('Microphone access requested.');
});

document.querySelector('#camera-btn').addEventListener('click', function() {
    alert('Camera access requested.');
});

// Sidebar toggle functionality
const sidebarToggle = document.querySelector('#sidebar-toggle');
const sidebar = document.querySelector('.sidebar');

sidebarToggle.addEventListener('click', function() {
    sidebar.style.left = sidebar.style.left === '0px' ? '-200px' : '0px';
});

// Example for notification button
document.querySelector('#notify-btn').addEventListener('click', function() {
    alert('You have no new notifications.');
});
