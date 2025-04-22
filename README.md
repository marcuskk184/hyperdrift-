
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
