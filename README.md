<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>مباريات برشلونة</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>مباريات برشلونة</h1>
    <nav>
      <ul>
        <li><a href="#home">الرئيسية</a></li>
        <li><a href="#matches">المباريات القادمة</a></li>
        <li><a href="#news">الأخبار</a></li>
        <li><a href="#login">تسجيل الدخول</a></li>
      </ul>
    </nav>
  </header>
  
  <section id="home">
    <h2>مرحبًا بك في موقع مباريات برشلونة!</h2>
    <p>هنا تجد آخر الأخبار والنتائج الخاصة بفريق برشلونة.</p>
  </section>

  <section id="matches">
    <h2>المباريات القادمة</h2>
    <ul>
      <li>برشلونة ضد ريال مدريد - 25 مارس 2025</li>
      <li>برشلونة ضد أتليتكو مدريد - 2 أبريل 2025</li>
      <li>برشلونة ضد فالنسيا - 10 أبريل 2025</li>
    </ul>
  </section>

  <section id="news">
    <h2>آخر الأخبار</h2>
    <ul>
      <li><a href="#">الإصابة تطارد أحد لاعبي برشلونة</a></li>
      <li><a href="#">برشلونة يحقق فوزًا كبيرًا في الدوري</a></li>
    </ul>
  </section>

  <footer>
    <p>جميع الحقوق محفوظة © 2025</p>
  </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <a href="https://www.fcbarcelona-live-news.com">my websied
  
  </a>
</body>
</html>

<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>تسجيل الدخول</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>تسجيل الدخول إلى حسابك</h1>
  </header>

  <section>
    <form id="loginForm">
      <label for="email">البريد الإلكتروني:</label>
      <input type="email" id="email" placeholder="أدخل بريدك الإلكتروني" required>

      <label for="password">كلمة المرور:</label>
      <input type="password" id="password" placeholder="أدخل كلمة المرور" required>

      <button type="submit">تسجيل الدخول</button>
    </form>

    <p>ليس لديك حساب؟ <a href="signup.html">أنشئ حسابًا جديدًا</a></p>
  </section>

  <footer>
    <p>جميع الحقوق محفوظة © 2025</p>
  </footer>

  <script src="firebase.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>إنشاء حساب</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>إنشاء حساب جديد</h1>
  </header>

  <section>
    <form id="signupForm">
      <label for="name">الاسم الكامل:</label>
      <input type="text" id="name" placeholder="أدخل اسمك الكامل" required>

      <label for="email">البريد الإلكتروني:</label>
      <input type="email" id="email" placeholder="أدخل بريدك الإلكتروني" required>

      <label for="password">كلمة المرور:</label>
      <input type="password" id="password" placeholder="أدخل كلمة المرور" required>

      <button type="submit">إنشاء حساب</button>
    </form>

    <p>هل لديك حساب؟ <a href="login.html">تسجيل الدخول</a></p>
  </section>

  <footer>
    <p>جميع الحقوق محفوظة © 2025</p>
  </footer>

  <script src="firebase.js"></script>
</body>
</html>

<script src="https://www.gstatic.com/firebasejs/9.0.0/firebase-app.js">head</script>
<script src="https://www.gstatic.com/firebasejs/9.0.0/firebase-auth.js">head</script>

const signupForm = document.getElementById("signupForm");
signupForm.addEventListener("submit", function(event) {
  event.preventDefault();

  const name = document.getElementById("name").value;
  const email = document.getElementById("email").value;
  const password = document.getElementById("password").value;

  firebase.auth().createUserWithEmailAndPassword(email, password)
    .then((userCredential) => {
      const user = userCredential.user;
      alert("تم إنشاء الحساب بنجاح");
    })
    .catch((error) => {
      alert("حدث خطأ: " + error.message);
    });
});

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    direction: rtl;
    background-color: #f4f4f4;
  }
  
  header {
    background-color: #0f4c75;
    color: white;
    padding: 20px;
    text-align: center;
  }
  
  nav ul {
    list-style-type: none;
    padding: 0;
  }
  
  nav ul li {
    display: inline;
    margin: 0 15px;
  }
  
  nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
  }
  
  section {
    padding: 20px;
    margin: 10px 0;
  }
  
  footer {
    text-align: center;
    padding: 10px;
    background-color: #0f4c75;
    color: white;
  }

  
