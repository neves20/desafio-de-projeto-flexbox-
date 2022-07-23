# desafio-de-projeto-flexbox-
meu primeiro projeto sobre sobre flexbox com html e css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Instagram</title>
</head>
<body>
    <div class="Facebook-wrapper">
        <div class="Facebook-phone">
            <img src="./img/png-transparent-smartphone-facebook-live-video-multimedia-mobile-phones-smartphone-gadget-electronics-display-advertising (2).jpg" alt="celular">
        </div>
        <div class="Facebook-continue">
            <div class="group">
                <img src="./img/Facebook_logo_(square).png" class="Facebook-logo" alt="Facebook logo">
                <div class="profile-photo">
                    <img src="./img/transferir.jfif" alt="foto de perfil">
                </div>
                <a href="#" class="Facebook-login">Continue como sprucegabriela</a>
                <a href="#" class="Facebook-logout">Remover conta</a>
            </div>
            <div class="group">
                <p class="not-account">Não é sprucegabriela?</p>
                <p class="not-account">
                    <span class="link-blue">Alternar contas</span>
                    ou
                    <span class="link-blue">Inscreva-se</span>
                </p>
            </div>
            <div class="get-the-app">
                <p class="get-app">Baixe o aplicativo</p>
                <div class="download">
                    <a href="#" class="app-download"></a>
                    <a href="#" class="app-download"></a>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    text-decoration: none;
    font-family: sans-serif;
    font-size: 14px;
}

body {
    width: 100%;
    min-height: 100vh;
    background-color: rgb(243, 243, 243);
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
}

.facebook-wrapper {
    display: flex;
    align-items: center;
    justify-content: start;
    width: 60%;
    height: 100vh;
}

.facebook-phone {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50%;
}

.facebook-phone img {
    height: 50rem;
}

.facebook-continue {
    display: flex;
    align-items: center; /* horizontal */
    justify-content: space-around; /* vertical */
    flex-direction: column;
    width: 50%;
    min-height: 34rem;
}

.group {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    background-color: #ffffff;
    width: 100%;
    padding: 1.3rem 0;
    border: 1px solid lightgray;
}

.group:nth-child(1) {
    min-height: 19rem;
}

.facebook-logo {
    height: 3rem;
}

.profile-photo {
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    overflow: hidden;
}

.profile-photo img {
    height: 6rem;
}

.facebook-login {
    background-color: #0095f6;
    color: #ffffff;
    padding: 8px;
    border-radius: 4px;
}

.facebook-logout {
    color: #0095f6;
    margin-top: 1rem;
}

.not-account {
    color: rgb(160, 160, 160);
}

.link-blue {
    color: #0095f6;
}

.get-the-app {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    padding: 1.3rem 0;
}

.download {
    display: flex;
    width: 100%;
    justify-content: space-evenly;
    align-items: center;
    padding: 1rem;
}

.app-download {
    height: 3rem;
    width: 10rem;
    background-size: cover;
}

.app-download:nth-child(1) {
    background-image: url('./img/transferir.png');
}

.app-download:nth-child(2) {
    background-image: url('./img/transferir (1).png');
}

/* media queries */


@media (max-width: 1024px) {
    .Facebook-wrapper {
        width: 90%;
    }
}

@media (max-width: 650px) {
    body {
        background-color: #ffffff;
    }

    .facebook-wrapper {
        width: 90%;
    }

    .facebook-phone {
        display: none;
    }

    .facebook-continue {
        width: 100%;
    }
    
    .group {
        border: 1px solid transparent;
    }
}
