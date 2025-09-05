quantum-quokka/
  ├── index.html
  ├── style.css
  ├── script.js
  └── assets/
       └── hero-banner.jpg (replace with your real image/logo)
       
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quantum Quokka ($QQOK) - The Happiest Meme Coin</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>
<header>
  <h1>Quantum Quokka ($QQOK)</h1>
  <nav>
    <a href="#about">About</a>
    <a href="#tokenomics">Tokenomics</a>
    <a href="#how-to-buy">How to Buy</a>
    <a href="#community">Community</a>
    <a href="#newsletter">Subscribe</a>
    <a href="#airdrop">Airdrop</a>
  </nav>
</header>

<div class="hero">
  <h1>Welcome to $QQOK - Quantum Smiles to the Moon!</h1>
</div>

<div id="about" class="section">
  <h2>About Quantum Quokka</h2>
  <p>Meet $QQOK, the happiest meme coin on the Solana blockchain! Inspired by the joyful quokka and powered by quantum computing vibes, $QQOK brings fun, innovation, and community to crypto. Launched on September 4, 2025, at 11:42 PM EDT, we’re here to redefine meme coins with a smile!</p>
</div>

<div id="tokenomics" class="section tokenomics">
  <h2>Tokenomics</h2>
  <ul>
    <li>Total Supply: 1,000,000,000 $QQOK</li>
    <li>60% - Community & Liquidity</li>
    <li>20% - Presale</li>
    <li>10% - Development</li>
    <li>10% - Marketing & Airdrops</li>
  </ul>
</div>

<div id="how-to-buy" class="section how-to-buy">
  <h2>How to Buy $QQOK</h2>
  <ol>
    <li>Set up a Solana wallet (e.g., Phantom).</li>
    <li>Buy SOL from an exchange (e.g., Binance, Coinbase).</li>
    <li>Connect to a Solana DEX like Raydium.</li>
    <li>Swap SOL for $QQOK using the official token address (TBA).</li>
    <li>Join our community for updates on listings!</li>
  </ol>
</div>

<div id="community" class="section community">
  <h2>Join the $QQOK Community</h2>
  <p>Follow us on:</p>
  <a href="#">X</a> | <a href="#">Telegram</a> | <a href="#">Discord</a>
  <p>Participate in our airdrop for a chance to win $QQOK tokens!</p>
</div>

<div id="newsletter" class="section">
  <h2>Subscribe for Updates</h2>
  <form id="signup-form">
    <input type="email" id="email" placeholder="Enter your email" required>
    <button type="submit">Subscribe</button>
    <p id="form-message"></p>
  </form>
</div>

<div id="airdrop" class="section">
  <h2>Airdrop Registration</h2>
  <form id="airdrop-form">
    <input type="text" id="wallet" placeholder="Enter Solana Wallet Address" required>
    <button type="submit">Register</button>
    <p id="airdrop-message"></p>
  </form>
</div>

<footer>
  <p>&copy; 2025 Quantum Quokka. Not financial advice. DYOR.</p>
  <p>Contact: support@quantumquokka.com</p>
</footer>
</body>
</html>

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: linear-gradient(135deg, #1e3c72, #2a5298);
  color: #fff;
  text-align: center;
}

header {
  background: #ff6f61;
  padding: 1rem;
}

nav a {
  color: #fff;
  margin: 0 1rem;
  text-decoration: none;
  font-weight: bold;
}

nav a:hover {
  color: #ffcc5c;
}

.hero {
  padding: 2rem;
  background: url('assets/hero-banner.jpg') no-repeat center/cover;
  height: 400px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero h1 {
  font-size: 3rem;
  text-shadow: 2px 2px 4px #000;
}

.section {
  padding: 2rem;
  max-width: 800px;
  margin: 0 auto;
}

.tokenomics, .how-to-buy, .community, #newsletter, #airdrop {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  margin-bottom: 2rem;
  padding: 1rem;
}

form input, form button {
  padding: 0.5rem;
  margin: 0.5rem;
  border: none;
  border-radius: 5px;
}

form input {
  width: 60%;
}

form button {
  background: #ff6f61;
  color: #fff;
  cursor: pointer;
}

form button:hover {
  background: #ffcc5c;
  color: #000;
}

footer {
  background: #ff6f61;
  padding: 1rem;
  position: fixed;
  bottom: 0;
  width: 100%;
}

@media (max-width: 600px) {
  .hero h1 {
    font-size: 2rem;
  }
}

// Smooth scroll
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function (e) {
    e.preventDefault();
    document.querySelector(this.getAttribute('href')).scrollIntoView({
      behavior: 'smooth'
    });
  });
});

// Newsletter signup validation
document.getElementById('signup-form').addEventListener('submit', function(e) {
  e.preventDefault();
  const email = document.getElementById('email').value.trim();
  const message = document.getElementById('form-message');

  if (/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
    message.textContent = "✅ Thanks for subscribing!";
    message.style.color = "#00ffcc";
    // TODO: send email to backend or Google Form
  } else {
    message.textContent = "❌ Please enter a valid email.";
    message.style.color = "#ff4444";
  }
});

// Airdrop wallet validation
document.getElementById('airdrop-form').addEventListener('submit', function(e) {
  e.preventDefault();
  const wallet = document.getElementById('wallet').value.trim();
  const msg = document.getElementById('airdrop-message');

  if (wallet.length >= 32) {
    msg.textContent = "✅ Registered! Stay tuned for airdrop results.";
    msg.style.color = "#00ffcc";
  } else {
    msg.textContent = "❌ Invalid Solana address.";
    msg.style.color = "#ff4444";
  }
});

