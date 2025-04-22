<!DOCTYPE html>
<html lang="da">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tøj & Sko Shop</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f8f9fa;
    }
    header {
      background-color: #222;
      color: #fff;
      padding: 1.5rem;
      text-align: center;
    }
    nav {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      background-color: #333;
      padding: 0.75rem;
    }
    nav a {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
    }
    .container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
      padding: 2rem;
    }
    .product {
      background-color: #fff;
      border-radius: 10px;
      padding: 1rem;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      text-align: center;
    }
    .product img {
      width: 100%;
      height: auto;
      border-radius: 6px;
    }
    .product h3 {
      margin: 0.5rem 0;
    }
    .product p {
      font-weight: bold;
    }
    .product button {
      background-color: #222;
      color: #fff;
      border: none;
      padding: 0.6rem 1.2rem;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .product button:hover {
      background-color: #555;
    }
    footer {
      background-color: #222;
      color: white;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }
    .cart {
      position: fixed;
      top: 20px;
      right: 20px;
      background-color: #fff;
      padding: 1rem;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
    }
  </style>
</head>
<body>
  <header>
    <h1>Tøj & Sko Shop</h1>
    <p>Din stil, dit valg</p>
  </header>

  <nav>
    <a href="#">Forside</a>
    <a href="#">Produkter</a>
    <a href="#">Kontakt</a>
  </nav>

  <main class="container">
    <div class="product">
      <img src="https://via.placeholder.com/250x250.png?text=Hættetrøje" alt="Hættetrøje">
      <h3>Hættetrøje</h3>
      <p>299 DKK</p>
      <button onclick="addToCart('Hættetrøje', 299)">Læg i kurv</button>
    </div>
    <div class="product">
      <img src="https://via.placeholder.com/250x250.png?text=Sneakers" alt="Sneakers">
      <h3>Sneakers</h3>
      <p>649 DKK</p>
      <button onclick="addToCart('Sneakers', 649)">Læg i kurv</button>
    </div>
    <div class="product">
      <img src="https://via.placeholder.com/250x250.png?text=Jeans" alt="Jeans">
      <h3>Jeans</h3>
      <p>399 DKK</p>
      <button onclick="addToCart('Jeans', 399)">Læg i kurv</button>
    </div>
  </main>

  <div class="cart" id="cart">
    <h3>🛒 Kurv</h3>
    <ul id="cart-items"></ul>
    <p><strong>Total:</strong> <span id="total">0</span> DKK</p>
  </div>

  <footer>
    <p>&copy; 2025 Tøj & Sko Shop. Alle rettigheder forbeholdes.</p>
  </footer>

  <script>
    const cartItems = document.getElementById("cart-items");
    const totalDisplay = document.getElementById("total");
    let total = 0;

    function addToCart(product, price) {
      const li = document.createElement("li");
      li.textContent = `${product} - ${price} DKK`;
      cartItems.appendChild(li);
      total += price;
      totalDisplay.textContent = total;
    }
  </script>
</body>
</html>
