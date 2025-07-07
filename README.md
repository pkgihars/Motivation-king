<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Avocardlo - Motivation for You</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #e0eafc, #cfdef3);
      color: #333;
    }

    .hero {
      text-align: center;
      padding: 100px 20px 60px;
      background: #2e86de;
      color: white;
    }

    .hero h1 {
      font-size: 4rem;
      font-weight: bold;
    }

    .hero p {
      font-size: 1.3rem;
      margin-top: 20px;
    }

    .quote-box {
      max-width: 800px;
      margin: 40px auto;
      padding: 30px;
      background-color: #ffffff;
      border-radius: 15px;
      box-shadow: 0px 10px 25px rgba(0, 0, 0, 0.1);
    }

    .quote {
      font-style: italic;
      font-size: 1.5rem;
    }

    .about, .contact {
      padding: 60px 20px;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #2e86de;
      color: white;
      margin-top: 50px;
    }

    .quote-author {
      margin-top: 15px;
      font-weight: bold;
      font-size: 1rem;
      color: #555;
    }
  </style>
</head>
<body>

  <!-- Hero Section -->
  <section class="hero">
    <h1>Avocardlo</h1>
    <p>Your daily dose of motivation and positivity</p>
  </section>

  <!-- Quote Rotator Section -->
  <section class="quote-box text-center">
    <div class="quote" id="quoteText">"Push yourself, because no one else is going to do it for you."</div>
    <div class="quote-author" id="quoteAuthor">– Unknown</div>
  </section>

  <!-- About Section -->
  <section class="about text-center">
    <div class="container">
      <h2>About Avocardlo</h2>
      <p>
        At Avocardlo, we believe that every day holds the opportunity for greatness. Whether you're chasing a dream, 
        fighting through a challenge, or just trying to stay inspired, our mission is to lift your spirit with carefully 
        chosen motivational thoughts and messages.
      </p>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="contact text-center">
    <div class="container">
      <h2>Contact Us</h2>
      <p>Want to share your thoughts or contribute a quote?</p>
      <p>Email: <a href="mailto:contact@avocardlo.com">contact@avocardlo.com</a></p>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    &copy; 2025 Avocardlo. Stay motivated. Stay powerful.
  </footer>

  <!-- JavaScript for Rotating Quotes -->
  <script>
    const quotes = [
      {
        text: "Believe you can and you're halfway there.",
        author: "– Theodore Roosevelt"
      },
      {
        text: "Success is not final, failure is not fatal: it is the courage to continue that counts.",
        author: "– Winston Churchill"
      },
      {
        text: "It always seems impossible until it’s done.",
        author: "– Nelson Mandela"
      },
      {
        text: "Don’t watch the clock; do what it does. Keep going.",
        author: "– Sam Levenson"
      },
      {
        text: "Dream it. Wish it. Do it.",
        author: "– Unknown"
      },
      {
        text: "Start where you are. Use what you have. Do what you can.",
        author: "– Arthur Ashe"
      }
    ];

    let index = 0;

    function showQuote() {
      const quoteElement = document.getElementById('quoteText');
      const authorElement = document.getElementById('quoteAuthor');
      quoteElement.innerText = `"${quotes[index].text}"`;
      authorElement.innerText = quotes[index].author;
      index = (index + 1) % quotes.length;
    }

    setInterval(showQuote, 5000); // Change quote every 5 seconds
  </script>
</body>
</html>
