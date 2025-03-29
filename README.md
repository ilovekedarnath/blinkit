<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Home</title>
        <style>
            body {
            font-family: 'Poppins', Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f9fa;
            background: url('https://images.pexels.com/photos/994605/pexels-photo-994605.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1') no-repeat center center fixed;
            background-size: cover;
            
        }
        
        header {
            background-color: #58b4ff;
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .nav-left img {
            height: 60px;
            max-width: 100%;
        }
        
        .nav-right {
            display: flex;
            align-items: center;
            justify-content: flex-end;
            flex-grow: 1;
        }
        
        .search-container {
            display: flex;
            align-items: center;
            background: white;
            padding: 12px;
            border-radius: 8px;
            max-width: 700px;
            margin: 20px auto;
            box-shadow: 0px 3px 10px rgba(0, 0, 0, 0.1);
            flex-grow: 1;
        }
        
        .search-container input {
            flex-grow: 1;
            padding: 12px;
            border: none;
            outline: none;
            font-size: 16px;
            border-radius: 8px;
        }
        
        .search-container button {
            padding: 12px;
            background-color: #28a745;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 8px;
            transition: 0.3s;
        }
        
        .search-container button:hover {
            background-color: #218838;
        }
        
        .icons img {
            width: 60px;
            height: auto;
        }
        
        h2 {
            background-color: #28a745;
            color: white;
            padding: 10px;
            border-radius: 5px;
            text-align: center;
        }
        
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            padding: 20px;
            justify-content: center;
            text-align: center;
        }
        
        .product {
            background: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
            position: relative;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .product:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
        
        .product img {
            width: 100%;
            max-width: 160px;
            height: 160px;
            object-fit: cover;
            display: block;
            margin: auto;
            border-radius: 10px;
            cursor: pointer;
            transition: opacity 0.3s;
        }
        
        .product:hover img {
            opacity: 0.8;
        }
        
        .product h3 {
            margin: 10px 0;
        }
        
        .add-to-cart {
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            padding: 10px;
            border: none;
            cursor: pointer;
            border-radius: 8px;
            transition: 0.3s;
        }
        
        .product:hover .add-to-cart {
            display: block;
        }
        
        .add-to-cart:hover {
            background-color: #ff4500;
        }
        
        ul {
            list-style-type: none;
            padding: 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        li {
            background: white;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }
        
        li img {
            width: 100px;
            height: auto;
            margin-bottom: 10px;
        }
        
        button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        
        .hidden {
            display: none;
        }
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f9fa;
        }
        
        .nav-right {
            display: flex;
            align-items: center;
            justify-content: flex-end;
            flex-grow: 1;
            gap: 20px; /* Adds spacing between cart and login */
        }
        
        .taskbar-icons {
            display: flex;
            align-items: center;
            gap: 20px; /* Adjust spacing as needed */
        }
        
        .taskbar {
            position: relative; /* Remove fixed position */
            top: auto;
            right: auto;
            background-color: white;
            padding: 10px 15px;
            border-radius: 20px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            display: flex;
            align-items: center;
        }
        
        
        .user-icon {
            cursor: pointer;
            display: flex;
            align-items: center;
        }
        
        .user-icon img {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.3);
        }
        
        /* Login Form */
        .container {
            display: none;
            position: absolute;
            top: 60px;
            right: 10px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }
        
        h2 {
            margin-bottom: 15px;
        }

        .input-group {
            text-align: left;
            margin-bottom: 15px;
        }

        .input-group label {
            display: block;
            font-size: 14px;
            margin-bottom: 5px;
        }

        .input-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 14px;
            outline: none;
            transition: border-color 0.3s ease-in-out;
        }

        .input-group input:focus {
            border-color: #007bff;
        }

        .password-container {
            position: relative;
        }

        .toggle-password {
            position: absolute;
            right: 10px;
            top: 50%;
            transform: translateY(-50%);
            cursor: pointer;
            color: #555;
            transition: color 0.3s ease-in-out;
        }

        .toggle-password:hover {
            color: #007bff;
        }

        .btn {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease-in-out;
        }

        .btn:hover {
            background-color: #0056b3;
        }

        .switch-text {
            margin-top: 10px;
            font-size: 14px;
        }

        .switch-text a {
            color: #007bff;
            cursor: pointer;
            text-decoration: none;
            transition: color 0.3s ease-in-out;
        }

        .switch-text a:hover {
            color: #0056b3;
            text-decoration: underline;
        }

        </style>
    </head>
    <body>
        <header>
            <div class="nav-left">
                <img src="https://clevertap.com/wp-content/uploads/2023/08/blinkit-logo_casestudy.png" alt="Blinkit Logo">
            </div>
            <div class="nav-right">
                <div class="search-container">
                    <input type="text" id="search-bar" placeholder="Search for products..." onkeyup="searchProduct()">
                    <button onclick="searchProduct()">🔍</button>
                </div>
            </div>
            <div class="taskbar-icons">
                <div class="icons">
                    <a href="cart.html">
                        <img src="https://images.vexels.com/media/users/3/200097/isolated/preview/942820836246f08c2d6be20a45a84139-shopping-cart-icon-shopping-cart.png" alt="Cart">
                    </a>
                </div>
            
                <div class="taskbar" id="taskbar">
                    <div class="user-icon" onclick="toggleForm()">
                        <img src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png" alt="User">
                    </div>
                </div>
            </div>
            

        <!-- Login/Signup Form -->
        <div class="container" id="form-container">
            <h2 id="form-title">Create account</h2>

            <div class="input-group">
                <label>Email</label>
                <input type="email" id="email" placeholder="Enter your email">
            </div>

            <div class="input-group password-container">
                <label>Password</label>
                <input type="password" id="password" placeholder="Enter your password">
                <span class="toggle-password" onclick="togglePassword()">👁️</span>
            </div>

            <button class="btn" onclick="submitForm()">Create account</button>

            <p class="switch-text">
                Have an account? <a id="switch-link" onclick="switchForm()">Log in</a>
            </p>
        </div>
        </header>
        <h2>Tea, Coffee & Health Drinks</h2>
        <div class="products" id="product-list">
            <div class="product">
                <img src="https://ikneadtoeat.com/wp-content/uploads/2019/01/Masala-Chai-Recipe-1.jpg" alt="Tea">
                <h3>Tea</h3>
                <p><strong>Price: $2.50</strong></p>
                <button class="add-to-cart" onclick="addToCart('Tea', 2.50)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://static.vecteezy.com/system/resources/thumbnails/025/282/026/small/stock-of-mix-a-cup-coffee-latte-more-motive-top-view-foodgraphy-generative-ai-photo.jpg" alt="Coffee">
                <h3>Coffee</h3>
                <p><strong>Price: $3.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Coffee', 3.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://c.ndtvimg.com/2023-10/j9q17m2g_drinks_625x300_22_October_23.jpg" alt="Health Drink">
                <h3>Health Drink</h3>
                <p><strong>Price: $4.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Health Drink', 4.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://www.eatingwell.com/thmb/bqrbfaeglB7Gy2Twiw5mRVfLVyI=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/8265029-f31794103dd7432d927a3ac95a9be6a7.jpg" alt="Vegan Drinks">
                <h3>Vegan Drinks</h3>
                <p><strong>Price: $5.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Vegan Drinks', 5.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://imgs.search.brave.com/lJq9VSJcv86EFlGPHxyUgbKI_BXjVJkoZOPXVGGckDM/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly90NC5m/dGNkbi5uZXQvanBn/LzAwLzgwLzgwLzAx/LzM2MF9GXzgwODAw/MTUzX21aaFBwSHVS/TE9JQ3hGZ21SaUg3/R092RUxKWjJCNExv/LmpwZw" alt="Green Tea">
                <h3>Green Tea</h3>
                <p><strong>Price: $3.50</strong></p>
                <button class="add-to-cart" onclick="addToCart('Green Tea', 3.50)">Add to Cart</button>
            </div>
        </div>
        <h2>Hair & Beauty</h2>
        <div class="products" id="product-list">
            <div class="product">
                <img src="https://media.istockphoto.com/id/1159037549/photo/beautiful-brown-haired-girl-with-a-perfectly-curls-hair-and-classic-make-up-beauty-face-and.jpg?s=612x612&w=0&k=20&c=yIkepJHens3SZFi4cobrgR-U_vXiFld88ewMotYfyeU=" alt="Hair Care">
                <h3>Hair Care</h3>
                <p><strong>Price: $10.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Hair Care', 10.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://cdn.britannica.com/35/222035-131-9FC95B31/makeup-cosmetics.jpg" alt="Beauty and Makeup">
                <h3>Beauty and Makeup</h3>
                <p><strong>Price: $15.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Beauty and Makeup', 15.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlo4RbaYxoUEjE2rpI7l-YSsyjA9UmYO57Ow&s" alt="Eyeliner">
                <h3>Eyeliner</h3>
                <p><strong>Price: $8.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Eyeliner', 8.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://images.ctfassets.net/wlke2cbybljx/6Z75K7EQh8g4FfDz4TrtyZ/db8c19ba086ca39a187640400ba323b3/LIPSTICKS_X10_Square_RGB.jpg" alt="Lipstick">
                <h3>Lipstick</h3>
                <p><strong>Price: $12.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Lipstick', 12.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://ponds.in/cdn/shop/articles/bg4.jpg?v=1675838422" alt="BB & CC Cream">
                <h3>BB & CC Cream</h3>
                <p><strong>Price: $20.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('BB & CC Cream', 20.00)">Add to Cart</button>
            </div>
        </div>

        <h2>Dairy, Bread & Eggs</h2>
        <div class="products" id="product-list">
            <div class="product">
                <img src="https://static.toiimg.com/thumb/msid-115029115,width-400,resizemode-4/115029115.jpg" alt="Cheese">
                <h3>Cheese</h3>
                <p><strong>Price: $5.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Cheese', 5.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSS0b6MhdcJ5M8XJY-S4tK_SOcf3xj2jluGXA&s" alt="Curd & Yogurt">
                <h3>Curd & Yogurt</h3>
                <p><strong>Price: $3.50</strong></p>
                <button class="add-to-cart" onclick="addToCart('Curd & Yogurt', 3.50)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://www.biggerbolderbaking.com/wp-content/uploads/2016/03/IMG_0593.jpg" alt="Condensed Milk">
                <h3>Condensed Milk</h3>
                <p><strong>Price: $4.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Condensed Milk', 4.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://rumkisgoldenspoon.com/wp-content/uploads/2021/06/Ladi-pav-recipe.jpg" alt="Buns & Pav">
                <h3>Buns & Pav</h3>
                <p><strong>Price: $2.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Buns & Pav', 2.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQKRc1vsNojeMRzLpjSF-_g3ihYlGBwVgpNqw&s" alt="Milk">
                <h3>Milk</h3>
                <p><strong>Price: $1.50</strong></p>
                <button class="add-to-cart" onclick="addToCart('Milk', 1.50)">Add to Cart</button>
            </div>
        </div>

        <h2>Cold Drinks & Juices</h2>
        <div class="products" id="product-list">
            <div class="product">
                <img src="https://indian-retailer.s3.ap-south-1.amazonaws.com/s3fs-public/2024-11/Untitled%20design%20%2843%29.jpg" alt="Energy Drinks">
                <h3>Energy Drinks</h3>
                <p><strong>Price: $4.50</strong></p>
                <button class="add-to-cart" onclick="addToCart('Energy Drinks', 4.50)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://images.immediate.co.uk/production/volatile/sites/30/2024/06/Coconut-water700-d717060.jpg?quality=90&fit=700,350" alt="Coconut Water">
                <h3>Coconut Water</h3>
                <p><strong>Price: $3.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Coconut Water', 3.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://c8.alamy.com/comp/KPMGM5/bangkok-thailand-chakphet-road-juice-concentrates-and-syrups-for-fruit-KPMGM5.jpg" alt="Concentrates & Syrups">
                <h3>Concentrates & Syrups</h3>
                <p><strong>Price: $5.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Concentrates & Syrups', 5.00)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQLBCMfK3IE1Tt8mSsXhImEtclsAdlYEHxHDQ&s" alt="Sharbat">
                <h3>Sharbat</h3>
                <p><strong>Price: $3.50</strong></p>
                <button class="add-to-cart" onclick="addToCart('Sharbat', 3.50)">Add to Cart</button>
            </div>
            <div class="product">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRFTMAWUlaT_w6PibUDr0-pmD-qzBKS8RiYzw&s" alt="Mango Juice">
                <h3>Mango Juice</h3>
                <p><strong>Price: $4.00</strong></p>
                <button class="add-to-cart" onclick="addToCart('Mango Juice', 4.00)">Add to Cart</button>
            </div>
        </div>

        <script>
            let cart = [];

            function addToCart(productName) {
                cart.push(productName);
                alert(productName + " added to cart!");
                console.log("Cart:", cart);
            }
            function searchProduct() {
                let query = document.getElementById("search-bar").value.toLowerCase();
                let products = document.querySelectorAll(".product");

                products.forEach(product => {
                    let name = product.getAttribute("data-name").toLowerCase();
                    if (name.includes(query)) {
                        product.style.display = "block";
                    } else {
                        product.style.display = "none";
                    }
                });
            }

            function showProducts(category) {
                alert("Showing products for: " + category);
            }
            let isLogin = false;

            function toggleForm() {
                let form = document.getElementById("form-container");
                form.style.display = (form.style.display === "block") ? "none" : "block";
            }

            function switchForm() {
                isLogin = !isLogin;
                document.getElementById("form-title").textContent = isLogin ? "Log in" : "Create account";
                document.querySelector(".btn").textContent = isLogin ? "Log in" : "Create account";
                document.getElementById("switch-link").textContent = isLogin ? "Sign up" : "Log in";
            }

            function togglePassword() {
                let passwordField = document.getElementById("password");
                passwordField.type = (passwordField.type === "password") ? "text" : "password";
            }

            function submitForm() {
                let email = document.getElementById("email").value;
                let password = document.getElementById("password").value;

                if (email === "" || password === "") {
                    alert("Please fill in all fields.");
                } else {
                    alert(isLogin ? "Logged in successfully!" : "Account created successfully!");
                    hideTaskbar();
                }
            }

            function hideTaskbar() {
                document.getElementById("taskbar").style.display = "none";
                document.getElementById("form-container").style.display = "none";
            }

            // Close form when clicking outside
            document.addEventListener("click", function(event) {
                let form = document.getElementById("form-container");
                let userIcon = document.querySelector(".user-icon");

                if (!form.contains(event.target) && !userIcon.contains(event.target)) {
                    form.style.display = "none";
                }
            });
            function addToCart(productName, price) {
                let cart = JSON.parse(localStorage.getItem('cart')) || [];

                // Check if item already exists in the cart
                let existingProduct = cart.find(item => item.name === productName);
                if (existingProduct) {
                    existingProduct.quantity += 1;
                } else {
                    cart.push({ name: productName, price: price, quantity: 1 });
                }

                localStorage.setItem('cart', JSON.stringify(cart));
                alert(productName + " added to cart!");
            }
        </script>
    </body>
</html>
