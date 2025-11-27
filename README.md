# Onestyle
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ONE STYLE | Modern & Streetwear Clothing</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- HEADER -->
    <header>
        <div class="logo">ONE STYLE</div>
        <nav>
            <a href="#home">Home</a>
            <a href="#products">Products</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <!-- HERO SECTION -->
    <section id="home" class="hero">
        <h1>ONE STYLE</h1>
        <p>Modern Dresses & Streetwear That Redefine Your Style.</p>
        <a href="#products" class="btn">Shop Now</a>
    </section>

    <!-- PRODUCTS -->
    <section id="products" class="products">
        <h2>Latest Collection</h2>

        <div class="product-grid">

            <!-- PRODUCT 1 -->
            <div class="product">
                <img src="https://via.placeholder.com/300x400" alt="Product">
                <h3>Oversized Street Tee</h3>
                <p class="price">₹699</p>
                <button class="pay-btn" onclick="payNow(699, 'Oversized Street Tee')">Buy Now</button>
            </div>

            <!-- PRODUCT 2 -->
            <div class="product">
                <img src="https://via.placeholder.com/300x400" alt="Product">
                <h3>Modern Black Hoodie</h3>
                <p class="price">₹1299</p>
                <button class="pay-btn" onclick="payNow(1299, 'Modern Black Hoodie')">Buy Now</button>
            </div>

            <!-- PRODUCT 3 -->
            <div class="product">
                <img src="https://via.placeholder.com/300x400" alt="Product">
                <h3>Women's Urban Dress</h3>
                <p class="price">₹999</p>
                <button class="pay-btn" onclick="payNow(999, 'Women's Urban Dress')">Buy Now</button>
            </div>

        </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="about">
        <h2>About One Style</h2>
        <p>ONE STYLE brings premium modern fashion mixed with bold streetwear vibes.  
        We focus on comfort, quality, and unique designs that make you stand out.</p>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <p>WhatsApp: +91 XXXXX XXXXX</p>
        <p>Email: onestylebrand@gmail.com</p>
    </section>

    <footer>
        <p>© 2025 ONE STYLE. All Rights Reserved.</p>
    </footer>


    <!-- PAYMENT GATEWAY (RAZORPAY) -->
    <script src="https://checkout.razorpay.com/v1/checkout.js"></script>

    <script>
        function payNow(amount, product) {
            var options = {
                "key": "rzp_test_1234567890ABCDE",  
                "amount": amount * 100, 
                "currency": "INR",
                "name": "ONE STYLE",
                "description": product,
                "image": "",
                "handler": function (response){
                    alert("Payment Successful! Payment ID: " + response.razorpay_payment_id);
                },
                "theme": {
                    "color": "#000000"
                }
            };
            var rzp1 = new Razorpay(options);
            rzp1.open();
        }
    </script>

</body>
</html>
