# Parallax con HTML y CSS

Proyecto realizado con el efecto Parallax con HTML y CSS, con el cual se logra un movimiento distinto entre las diferentes figuras existentes dentro de la pagina.

![preview](https://raw.githubusercontent.com/juliolh0686/parallax-css/master/preview.jpg)

>Codigo HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./assets/css/style.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@900&display=swap" rel="stylesheet">
</head>
<body>
    <div class="mobil"><h1>No Soportado</h1></div>
    <div class="parallax-container">
        <div class="image image--background">
            <img src="./assets/img/Fondo.jpg" alt="background">
        </div>
        <div class="text">
            <h1>ESCAPATE DE LA CIUDAD</h1>
        </div>
        <div class="image image--personaje">
            <img src="./assets/img/persona.png" alt="personaje">
        </div>
    </div>
</body>
</html>

```
>Codigo CSS
```css
body {
  margin: 0;
  padding: 0;
  font-family: 'Roboto', sans-serif;
}

.mobil {
  display: none;
}

.parallax-container {
  width: 100%;
  height: 100vh;
  -webkit-perspective: 8px;
          perspective: 8px;
  -webkit-perspective-origin: 50%;
          perspective-origin: 50%;
  overflow-x: hidden;
  overflow-y: scroll;
  position: relative;
}

.parallax-container .image {
  position: absolute;
  margin: 0 auto;
  -webkit-transform: 0 50%;
          transform: 0 50%;
}

.parallax-container .image--background {
  width: 100%;
  height: 100%;
  -webkit-transform: translate(0px) scale(1);
          transform: translate(0px) scale(1);
}

.parallax-container .image--background img {
  width: 100%;
}

.parallax-container .image--personaje {
  width: 60%;
  top: 32%;
  right: 28%;
  -webkit-transform: translateZ(1px) scale(0.87);
          transform: translateZ(1px) scale(0.87);
  -webkit-transform-origin: bottom;
          transform-origin: bottom;
}

.parallax-container .image--personaje img {
  width: 100%;
}

.parallax-container .text {
  top: 15%;
  position: absolute;
  width: 100%;
  text-align: center;
  margin-top: 10%;
  font-size: 20px;
  color: #FFC078;
  font-weight: bold;
  -webkit-transform: translateZ(2px) scale(0.87);
          transform: translateZ(2px) scale(0.87);
  -webkit-transform-origin: bottom;
          transform-origin: bottom;
}

@media (max-width: 1100px) {
  .parallax-container {
    display: none;
  }
  .mobil {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    width: 100%;
    height: 100vh;
    color: white;
    text-align: center;
    background-color: #636262;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
  }
  .mobil h1 {
    margin: 0 auto;
  }
}

@media (min-width: 1500px) {
  .parallax-container .image--personaje {
    top: 40%;
  }
}

@media (min-width: 1820px) {
  .parallax-container .image--personaje {
    top: 60%;
  }
}

```

Creado por: Julio Loarte Huerto