# Project-1

Font Awasome 
===
    <!-- Font Awasome -->
    <script src="https://kit.fontawesome.com/1d23864fb5.js" crossorigin="anonymous"></script>

Google Fonts 
===
   <!-- Google - Font -->
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat&display=swap" rel="stylesheet">
===
Bootstap (v5.3)
   <!--Bootstrap CSS  -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

       <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
        crossorigin="anonymous"></script> 
---

---
Navbar
https://getbootstrap.com/docs/5.3/components/navbar/
+ position-sticky top-0
+ navbar-nav ms-auto
- fluid
- bg-body-tertiary
-                    <li class="nav-item">
                        <a class="nav-link disabled" aria-disabled="true">Disabled</a>
                    </li>
---


===
HTML (index.html)
---
https://fontawesome.com/icons/bars?f=classic&s=solid
-                   <span class="navbar-toggler-icon"></span>
+                   <i class="fa-solid fa-bars"></i>
+               <i class="fa-solid fa-headset"></i>
- Navbar - zaminana nazwy na ikonę i dodaję nazwę PROGAMERS
+  dodanie dodatkowych nav-link (o nas; portfolio; cena; zespół; osiągnięcia; kontakt)
---

===
CSS(Scss) (main.scss)(_colors.scss)
---
+                     nav {
+                       text-transform : uppercase;
+                       .nav-link, .navbar-nav .nav-link.active, .navbar-nav .show>.nav-link, .navbar-brand, .fa-bars {
                            color: #fff;
                    
+                        .nav-link:focus, .nav-link:hover, .navbar-nav .nav-link.active, .navbar-nav .show>.nav-link {
+                         color: #039dff;
+                         z-index:5;       #Zapobiega przykrywaniu nawigacji
                          }
                      }
+  (_colors.scss)
+        $main-color: #039dff;
          $white-color: #fff;

+  (main.scss)
+  @use './colors' as *;
+          color: $white-color;
+           color: $main-color;
---
HEADER
---
+     header.hero-img {
+         position:relative;
+         height:100vh;
+         backgroung-image: url("../img/hero-small.jpeg");
+         background-size: cover;
+         background-position: center;

 !! Problemy ze wsparciem np: Safarii !!
+         background-attachment: fixed;
  
+          color: $white;
+         z-index: 0;    #CIEŃ(1)
+          h1 {
+             text-transform: uppercase;
+         }
+      }

+     .hero-shadow {
+        position: absolute;
+        top: 0;
+        left: 0;
+        width: 100%;
+        height: 100%;
+        background-color: rgb(0,0,0,.8);
+        z-index: -5;   #CIEŃ(1)
+     }
WYŚRODKOWANIE TEKSTU NA STRONIE (domyślnie jest flex-direction row ⚠️)
+     .hero-text {
+        display: flex;
+        justyfy-content: center;
+        align-items: center;
+        flex-direction: column    #Trzeba dodać by wyśrodkować tekst
+        height: 100%;
      }
ZAMIANA KOLORU GAMERS
+        .blue-text {
+        color: $main.color;
+    }

===
JS (script.js)
---


===
MOBILE - CORECT 📱iPhone 5/SE ✅ Samsung Galaxy S8+📱✅ iPadPro📱✅ 
===
