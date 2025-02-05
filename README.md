<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant Menu</title>
   <style>
    body { 
        font-family: Arial, sans-serif;
        text-align: center; 
        background-image:url(olive.jpg);
        transition: background-image 0.5s ease-in-out;
    }
    .rn{
        padding-bottom: 0%;
        background-color: rgb(236, 167, 39);
        height: 20%;
        text-align: initial;
        justify-content:space-around;
        animation: fadeIn 2s;
    }
    .menu { 
        width: 68%; 
        margin: 0px 100px 10px 100px;
        display: flex;
        flex-wrap: wrap;
        gap: 20px; 
        border: 5px solid #eedcaf; 
        padding: 10px; 
        border-radius: 5px;
        justify-content: center;
        background-image: url('wooden-table.jpg'); 
        background-size: cover; 
        background-position: center; 
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); 
        animation: fadeIn 2s;
    }
    .menu-item { 
        display: flex;
        flex-direction: column;
        align-items: center;
        border: 3px solid rgb(87, 82, 82);
        background-color: #eedcaf; 
        padding: 10px;
        border-radius: 15px;
        justify-content: space-evenly;
        flex: 1 0 200px; 
        margin: 5px;
        text-align: center;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); 
        animation: fadeIn 2s;
    }
    button { 
        background: rgb(236, 167, 39); 
        color: rgb(10, 10, 10); 
        border: 2px solid black; 
        padding: 5px 10px; 
        cursor: pointer; 
        transition: background-color 0.5s ease-in-out;
    }
    button:hover {
        background-color: rgba(81, 96, 121, 0.267);
    }
    #cart { 
        height: 65%;
        justify-content: space-evenly;
        flex: 1 0 200px;
        margin: 15%;
        padding-bottom: 20px; 
        border: 1px solid whitesmoke;
        background-color: transparent; 
        color: whitesmoke;
        display: block;
        font-size: large;
        animation: fadeIn 2s;
    }
    .remove-button { 
        background: red; 
        color: white; 
        border: none; 
        padding: 5px 10px; 
        cursor: pointer; 
        transition: background-color 0.5s ease-in-out;
    }
    .remove-button:hover {
        background-color: rgb(255, 0, 0);
    }
    #indian,#chinese,#italian,#desserts{
        display: none;
    }
    h1{
        text-align: center;
        color: rgb(5, 9, 9);
        margin: 10%;
        justify-content: space-around;
        animation: fadeIn 2s;
    }
    .video {
        border: 5px solid white;
        position: relative;
        width: 100%;
        height: 300px;
        overflow: hidden;
        margin: 0 auto;
        animation: fadeIn 2s;
    }
    .video video {
        
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .video .overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        font-size: 24px;
        font-weight: bold;
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    }
    #indian-button,#chinese-button,#italian-button,#desserts-button{
        margin: 5%;
        animation: fadeIn 2s;
    }
    @keyframes fadeIn {
        0% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }
   </style>
</head>
<body>
    <div class="rn"><header>
    <h1>
    <img src="logo.png" height="50px" width="100px">Restaurant Menu</h1>
    
</header>
</div>
<button id="indian-button" onclick="showMenu('indian')">INDIAN</button>
<div class="audio">
    <audio autoplay loop>
        <source src="audio.mp3" controls>
    </audio>
</div>
<div id="indian">
    <div class="menu">
        
        <div class="menu-item">
            <img src="biryani.jpg" height="150px" width="150px" >
            <span>Biryani - $5</span>
            <button class="add-to-cart" data-item="Biryani" data-price="5">Add</button>
        </div>
        <div class="menu-item">
            <img src="chole.jpg" height="150px" width="150px">
            <span>Chole Bhature - $8</span>
            <button class="add-to-cart" data-item="Chole Bhature" data-price="8">Add</button>
        </div>
        <div class="menu-item">
            <img src="paneer.jpg" height="150px" width="150px">
            <span>Paneer Tikka - $7</span>
            <button class="add-to-cart" data-item="Paneer Tikka" data-price="7">Add</button>
        </div>
        <div class="menu-item">
            <img src="panipuri.jpg" height="150px" width="150px">
            <span>Pani puri - $7</span>
            <button class="add-to-cart" data-item="panipuri" data-price="7">Add</button>
        </div>
        <div class="menu-item">
            <img src="gulab jamun.jpg" height="150px" width="150px">
            <span>Gulab Jamun - $7</span>
            <button class="add-to-cart" data-item="gulab jamun" data-price="7">Add</button>
        </div>
        <div class="menu-item">
            <img src="kulfi.jpg" height="150px" width="150px">
            <span>kulfi - $7</span>
            <button class="add-to-cart" data-item="kulfi" data-price="7">Add</button>
        </div>



    </div>
    </div>
<button id="chinese-button" onclick="showMenu('chinese')">CHINESE</button>
<div id="chinese">
    <div class="menu">
        <div class="menu-item">
            <img src="dumpling.jpg" height="150px" width="150px">
            <span>dumpling - $5</span>
            <button class="add-to-cart" data-item="dumpling" data-price="5">Add</button>
        </div>
        <div class="menu-item">
            <img src="chowmeen.jpg" height="150px" width="150px">
            <span>chowmeen - $8</span>
            <button class="add-to-cart" data-item="chowmeen" data-price="8">Add</button>
        </div>
        <div class="menu-item">
            <img src="gobi.jpg" height="150px" width="150px">
            <span>Gobi Manchurian- $7</span>
            <button class="add-to-cart" data-item="gobi" data-price="7">Add</button>
        </div>
        <div class="menu-item">
            <img src="dumpling soup.jpg" height="150px" width="150px">
            <span>Dumpling Soup- $7</span>
            <button class="add-to-cart" data-item="soup" data-price="7">Add</button>
        </div>
    
    
    </div>
    </div>
<button id="italian-button" onclick="showMenu('italian')">ITALIAN</button>
<div id="italian">
        <div class="menu">
            <div class="menu-item">
                <img src="Pizza.jpeg" height="150px" width="150px">
                <span>Pizza - $5</span>
                <button class="add-to-cart" data-item="pizza" data-price="5">Add</button>
            </div>
            <div class="menu-item">
                <img src="pasta.jpeg" height="150px" width="150px">
                <span>Pasta - $8</span>
                <button class="add-to-cart" data-item="pasta" data-price="8">Add</button>
            </div>
            <div class="menu-item">
                <img src="mazarella.jpg" height="150px" width="150px">
                <span>Mozarella coctail- $7</span>
                <button class="add-to-cart" data-item="mozarella" data-price="7">Add</button>
            </div>
           
        
        
        </div>
        </div>
<button id="desserts-button" onclick="showMenu('desserts')">DESSERTS</button>
<div id="desserts">
    <div class="menu">
        <div class="menu-item">
            <img src="caramel.jpg" height="150px" width="150px">
            <span>caramel - $5</span>
            <button class="add-to-cart" data-item="caramel" data-price="5">Add</button>
        </div>
        <div class="menu-item">
            <img src="cookie.jpg" height="150px" width="150px">
            <span>Cookie - $8</span>
            <button class="add-to-cart" data-item="cookie" data-price="8">Add</button>
        </div>
        <div class="menu-item">
            <img src="mango.jpg" height="150px" width="150px">
            <span>Mango icecream - $7</span>
            <button class="add-to-cart" data-item="mango" data-price="7">Add</button>
        </div>
        <div class="menu-item">
            <img src="strawberry.jpg" height="150px" width="150px">
            <span>strawberry - $7</span>
            <button class="add-to-cart" data-item="strawberry" data-price="7">Add</button>
        </div>
    </div>
</div>
    
    <div id="cart">
       

        <h2>Cart</h2>
       
       
        <ul id="cart-items"></ul>
        <p>Total: $<span id="total">0</span></p>
        <button id="checkout-button">Checkout</button>
    </div>
    
    <script>
        let total = 0;
        const cartItems = document.getElementById('cart-items');
        const totalElement = document.getElementById('total');
        const checkoutButton = document.getElementById('checkout-button');
        
        document.addEventListener('DOMContentLoaded', () => {
            const addToCartButtons = document.querySelectorAll('.add-to-cart');
            addToCartButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const item = button.dataset.item;
                    const price = parseInt(button.dataset.price);
                    addToCart(item, price);
                });
            });
            
            checkoutButton.addEventListener('click', () => {
                if (total > 0) {
                    alert('Thank you for your order!');
                    cartItems.innerHTML = '';
                    total = 0;
                    totalElement.textContent = total;
                } else {
                    alert('Your cart is empty!');
                }
            });
        });
        
        function addToCart(item, price) {
            const newItem = document.createElement('li');
            newItem.textContent = `${item} - $${price}`;
            const removeButton = document.createElement('button');
            removeButton.textContent = 'Remove';
            removeButton.classList.add('remove-button');
            removeButton.addEventListener('click', () => {
                removeItem(newItem, price);
            });
            newItem.appendChild(removeButton);
            cartItems.appendChild(newItem);
            
            total += price;
            totalElement.textContent = total;
        }
        
        function removeItem(item, price) {
            item.remove();
            total -= price;
            totalElement.textContent = total;
        }
        
        function showMenu(menu) {
            const indianMenu = document.getElementById('indian');
            const chineseMenu = document.getElementById('chinese');
            const italianMenu = document.getElementById('italian');
            const dessertsMenu = document.getElementById('desserts');
            
            indianMenu.style.display = 'none';
            chineseMenu.style.display = 'none';
            italianMenu.style.display = 'none';
            dessertsMenu.style.display = 'none';
            
            if (menu === 'indian') {
                indianMenu.style.display = 'block';
            } else if (menu === 'chinese') {
                chineseMenu.style.display = 'block';
            } else if (menu === 'italian') {
                italianMenu.style.display = 'block';
            } else if (menu === 'desserts') {
                dessertsMenu.style.display = 'block';
            }
        }
    </script>
    <footer>
        <div class="video">
            <video autoplay loop muted plays-inline> 
                <source src="video.mp4" type="video/mp4">
            </video>
            <div class="overlay">
                <pre>Enjoy your meal!</pre>
            </div>
        </div>
        
    </footer>
</body>
</html>
