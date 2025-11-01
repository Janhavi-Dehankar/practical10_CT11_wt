# practical10_CT11_wt
contains web technology practical 10
Index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Foodify | Home</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">Foodify 🍕</div>
      <ul>
        <li><a href="index.html" class="active">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="cart.html">Cart</a></li>
        <li><a href="order.html">Order</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <h1>Delicious Food, Delivered Fresh!</h1>
    <p>Order your favorite meals anytime, anywhere with Foodify.</p>
    <a href="menu.html" class="btn">Order Now</a>
  </section>
</body>
</html>

Menu.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Foodify | Menu</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>
    <image url=""></image>
  <header>
    <nav class="navbar">
      <div class="logo">Foodify 🍕</div>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html" class="active">Menu</a></li>
        <li><a href="cart.html">Cart</a></li>
        <li><a href="order.html">Order</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="menu-section">
    <h2>Our Menu</h2>
    <div id="menu-container" class="menu-container"></div>
  </section>
</body>
</html>

Cart.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Foodify | Cart</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">Foodify 🍕</div>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="cart.html" class="active">Cart</a></li>
        <li><a href="order.html">Order</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="cart-section">
    <h2>Your Cart</h2>
    <div id="cart-items"></div>
    <p id="cart-total"></p>
    <a href="order.html" class="btn">Proceed to Order</a>
  </section>
</body>
</html>

Order.hml

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Foodify | Order</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">Foodify 🍕</div>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="cart.html">Cart</a></li>
        <li><a href="order.html" class="active">Order</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="order-form">
    <h2>Place Your Order</h2>
    <form id="orderForm" onsubmit="return validateOrderForm()">
      <label>Name:</label>
      <input type="text" id="name" required>

      <label>Email:</label>
      <input type="email" id="email" required>

      <label>Address:</label>
      <textarea id="address" required></textarea>

      <label>Phone:</label>
      <input type="text" id="phone" required>

      <button type="submit" class="btn">Confirm Order</button>
    </form>
  </section>
</body>
</html>

Contact.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Foodify | Contact</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">Foodify 🍕</div>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="cart.html">Cart</a></li>
        <li><a href="order.html">Order</a></li>
        <li><a href="contact.html" class="active">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="contact-section">
    <h2>Contact Us</h2>
    <form id="contactForm" onsubmit="return validateContactForm()">
      <label>Name:</label>
      <input type="text" id="cname" required>

      <label>Email:</label>
      <input type="email" id="cemail" required>

      <label>Message:</label>
      <textarea id="cmessage" required></textarea>

      <button type="submit" class="btn">Send Message</button>
    </form>
  </section>
</body>
</html>


Style.css

/* 🌈 Google Font */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap');

/* 🌐 General Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
  position: relative;
  z-index: 1;
}

body {
  
  background: #fff7f2;
  color: #333;
}

body::before
{
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.4);
    z-index: 0;
}

/* 🧭 Navbar */
.navbar {
  background: linear-gradient(90deg, #ff7043, #ff5722);
  color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 50px;
  position: sticky;
  top: 0;
  z-index: 100;
}

.navbar .logo {
  font-size: 1.5em;
  font-weight: 600;
}

.navbar ul {
  list-style: none;
  display: flex;
  gap: 25px;
}

.navbar ul li a {
  color: #fff;
  text-decoration: none;
  font-weight: 500;
  transition: 0.3s;
}

.navbar ul li a:hover,
.navbar ul li a.active {
  color: #ffd180;
}

/* 🏠 Hero Section */
.hero {
    
  height: 85vh;
  background: url(bg.jpeg) no-repeat center/cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
}

.hero h1 {
  font-size: 3rem;
  text-shadow: 2px 2px 8px rgba(0,0,0,0.5);
}

.hero p {
  font-size: 1.2rem;
  margin: 15px 0;
}

.btn {
  display: inline-block;
  padding: 12px 30px;
  background: #ff5722;
  color: #fff;
  border: none;
  border-radius: 30px;
  text-decoration: none;
  transition: 0.3s;
  cursor: pointer;
}

.btn:hover {
  background: #e64a19;
  transform: scale(1.05);
}

/* 🍕 Menu Page */
.menu-section {
  background: url(bg.jpeg) no-repeat center/cover;
  text-align: center;
  padding: 50px 20px;
}

.menu-section h2 {
  color: #ff5722;
  margin-bottom: 20px;
  font-size: 2rem;
}

.menu-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 25px;
  padding: 20px 50px;
}

.menu-item {
  background: #fff;
  border-radius: 15px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  padding: 15px;
  transition: 0.3s;
}

.menu-item img {
  width: 100%;
  border-radius: 10px;
}

.menu-item:hover {
  transform: translateY(-5px);
}

.menu-item h3 {
  color: #ff5722;
  margin: 10px 0;
}

.menu-item button {
  background: #ff7043;
  border: none;
  color: white;
  padding: 8px 15px;
  border-radius: 20px;
  cursor: pointer;
  transition: 0.3s;
}

.menu-item button:hover {
  background: #e64a19;
}

/* 🛒 Cart Page */
.cart-section {
  background: url(bg.jpeg) no-repeat center/cover;
  text-align: center;
  padding: 50px 20px;
}

#cart-items {
  margin-top: 20px;
}

.cart-item {
  background: #fff;
  border-radius: 12px;
  padding: 15px;
  margin: 10px auto;
  width: 60%;
  box-shadow: 0 3px 6px rgba(0,0,0,0.1);
  display: flex;
  justify-content: space-between;
}

#cart-total {
  font-weight: 600;
  margin: 20px 0;
  font-size: 1.3rem;
  color: #ff5722;
}

/* 🧾 Order Page */
.order-form {
  padding: 50px;
  max-width: 500px;
  margin: 0 auto;
  background: #fff;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.order-form form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.order-form input,
.order-form textarea {
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 10px;
  outline: none;
  transition: 0.3s;
}

.order-form input:focus,
.order-form textarea:focus {
  border-color: #ff5722;
  box-shadow: 0 0 5px rgba(255,87,34,0.5);
}

/* 📞 Contact Page */
.contact-section {
  padding: 50px;
  max-width: 500px;
  margin: 0 auto;
  background: #fff;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.contact-section form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.contact-section input,
.contact-section textarea {
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 10px;
  transition: 0.3s;
}

.contact-section input:focus,
.contact-section textarea:focus {
  border-color: #ff7043;
  box-shadow: 0 0 5px rgba(255,112,67,0.5);
}

/* 📱 Responsive */
@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    padding: 20px;
  }

  .navbar ul {
    flex-direction: column;
    gap: 15px;
  }

  .cart-item {
    width: 90%;
    flex-direction: column;
    align-items: center;
  }
}

script.js

// ===== Load Menu Items from XML =====
document.addEventListener("DOMContentLoaded", function () {
  const menuContainer = document.getElementById("menu-container");
  if (menuContainer) loadMenu();
  if (document.getElementById("cart-items")) displayCart();
});

// 🥗 Load menu items from foods.xml
function loadMenu() {
  fetch("foods.xml")
    .then((response) => response.text())
    .then((xmlText) => {
      const parser = new DOMParser();
      const xmlDoc = parser.parseFromString(xmlText, "application/xml");
      const items = xmlDoc.getElementsByTagName("food");

      const menuContainer = document.getElementById("menu-container");
      menuContainer.innerHTML = "";

      for (let i = 0; i < items.length; i++) {
        let name = items[i].getElementsByTagName("name")[0].textContent;
        let price = items[i].getElementsByTagName("price")[0].textContent;
        let image = items[i].getElementsByTagName("image")[0].textContent;

        const card = document.createElement("div");
        card.classList.add("menu-item");
        card.innerHTML = `
          <img src="${image}" alt="${name}">
          <h3>${name}</h3>
          <p>₹${price}</p>
          <button onclick="addToCart('${name}', ${price})">Add to Cart</button>
        `;
        menuContainer.appendChild(card);
      }
    })
    .catch((error) => console.log("Error loading XML:", error));
}

// ===== CART FUNCTIONS =====
let cart = JSON.parse(localStorage.getItem("cart")) || [];

function addToCart(name, price) {
  const existing = cart.find((item) => item.name === name);
  if (existing) {
    existing.qty += 1;
  } else {
    cart.push({ name, price, qty: 1 });
  }
  localStorage.setItem("cart", JSON.stringify(cart));
  alert(`${name} added to cart!`);
}

function displayCart() {
  const cartContainer = document.getElementById("cart-items");
  const totalElement = document.getElementById("cart-total");
  cart = JSON.parse(localStorage.getItem("cart")) || [];

  cartContainer.innerHTML = "";
  let total = 0;

  if (cart.length === 0) {
    cartContainer.innerHTML = "<p>Your cart is empty 😢</p>";
    totalElement.textContent = "";
    return;
  }

  cart.forEach((item, index) => {
    total += item.price * item.qty;
    const div = document.createElement("div");
    div.classList.add("cart-item");
    div.innerHTML = `
      <span>${item.name} (x${item.qty}) - ₹${item.price * item.qty}</span>
      <button onclick="removeFromCart(${index})">Remove</button>
    `;
    cartContainer.appendChild(div);
  });

  totalElement.textContent = `Total: ₹${total}`;
}

function removeFromCart(index) {
  cart.splice(index, 1);
  localStorage.setItem("cart", JSON.stringify(cart));
  displayCart();
}

// ===== FORM VALIDATION =====
function validateOrderForm() {
  const name = document.getElementById("name").value.trim();
  const email = document.getElementById("email").value.trim();
  const address = document.getElementById("address").value.trim();
  const phone = document.getElementById("phone").value.trim();

  if (name === "" || email === "" || address === "" || phone === "") {
    alert("All fields are required!");
    return false;
  }

  const phonePattern = /^[6-9][0-9]{9}$/;
  if (!phonePattern.test(phone)) {
    alert("Enter a valid 10-digit phone number!");
    return false;
  }

  alert("Order placed successfully! 🥳");
  localStorage.removeItem("cart");
  return true;
}

function validateContactForm() {
  const name = document.getElementById("cname").value.trim();
  const email = document.getElementById("cemail").value.trim();
  const message = document.getElementById("cmessage").value.trim();

  if (name === "" || email === "" || message === "") {
    alert("Please fill out all fields!");
    return false;
  }

  alert("Message sent successfully 💌");
  return true;
}

foods.xml

<?xml version="1.0" encoding="UTF-8"?>
<foods>
  <food>
    <name>Margherita Pizza</name>
    <price>299</price>
    <image>https://cdn.pixabay.com/photo/2017/12/09/08/18/pizza-3007395_1280.jpg</image>
  </food>

  <food>
    <name>Veg Burger</name>
    <price>149</price>
    <image>https://cdn.pixabay.com/photo/2014/10/23/18/05/burger-500054_1280.jpg</image>
  </food>

  <food>
    <name>Paneer Tikka</name>
    <price>199</price>
    <image>tikki.jpeg</image>
  </food>

  <food>
    <name>Momos</name>
    <price>129</price>
    <image>momos.jpeg</image>
  </food>

  <food>
    <name>Masala Dosa</name>
    <price>179</price>
    <image>dosa.jpeg</image>
  </food>

  <food>
    <name>Cold Coffee</name>
    <price>99</price>
    <image>coffee.jpeg</image>
  </food>
</foods>
