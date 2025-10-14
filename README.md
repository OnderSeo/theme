*,
*::after,
**::before {
    box-sizing: border-box;
}

:root {
    --orange: #FDC730;
    --cubic: cubic-bezier(0.4, 0, 0.2, 1);
}

.orange {
    color: var(--orange)
}

body {
    line-height: 1.5;
    padding: 0;
    margin: 0;
    background-image: url('../img/bg.png');
    background-position: top center;
    background-repeat: no-repeat;
    font-family: "Open Sans", Arial, Helvetica, sans-serif;
}

img {
    max-width: 100%;
}

a {
    color: inherit;
    text-decoration: none;
}

ul,
li {
    padding: 0;
    margin: 0;
    list-style-type: none;
}

.container {
    max-width: 1400px;
    width: 100%;
    margin-left: auto;
    margin-right: auto;
    position: relative;
}


/* Header */

.header {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    background: linear-gradient(to left, transparent 0%, rgb(28 31 44 / 0.7) 20%, rgb(28 31 44 / 1) 50%, rgb(28 31 44 / 0.7) 80%, transparent 100%);
    margin-top: 6em
}

.header::after {
    content: "";
    position: absolute;
    top: -4px;
    left: 0;
    width: 100%;
    height: 4px;
    background: linear-gradient(to left, transparent 0%, #FDC730 20%, #FDC730, #FDC730 80%, transparent 100%);
    z-index: 1;
}

.logo {
    position: relative;
    z-index: 3;
    margin-top: -2.5em;
    transform: translateY(1em)
}

.logo img {
    width: 300px;
}

.logoback {
    position: absolute;
    bottom: -1.5em;
    width: 400px;
    height: 100%;
    background: rgb(28 31 44 / 0.85);
    clip-path: polygon(0 0, 100% 0, 95% 100%, 5% 100%);
    z-index: 1;
    backdrop-filter: blur(5px);
}

.header .container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}

.header ul {
    position: absolute;
    right: 0;
    display: grid;
    grid-template-columns: auto auto;
}

.header ul li {
    transform: skew(-11deg);
    position: relative;
}

.header ul li a {
    padding: 1.75em 2em;
    color: #fff;
    position: relative;
    transform: skew(11deg);
    font-weight: 700;
}

.header ul li:first-child a {
    background: #e8b730;
}

.header ul li:last-child a {
    background: #1c1f2c;
}


/* Header Text */

.header-text {
    color: #fff;
    margin-top: 8em
}

.header-text .container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.header-text .container>* {
    max-width: 400px;
}

.header-text h1 {
    position: relative;
    font-size: 40px;
    font-weight: 600;
    line-height: 1.2;
    padding-left: .5em;
    margin: 0
}

.header-text h1::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    height: 70%;
    width: 4px;
    background: #FDC730;
}

.header-text p {
    text-align: right;
    font-weight: 400;
    margin: 0
}


/* Second Area */

.second-area {
    margin-top: 20em;
    color: #fff;
    text-align: center;
    background-image: url('../img/secondbg.png');
    background-position: top center;
    height: 1000px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.second-area .container {
    margin-top: 20em
}

.second-area h2 {
    font-size: 2em;
    margin: 0 0 .5em 0
}

.second-area p {
    max-width: 80%;
    margin: 0 auto;
    font-size: 1.1em;
}


/* Games Area */

.games-area {
    background-image: url('../img/gamesbg.png');
    background-size: 100% calc(100% - 3em);
    background-repeat: no-repeat;
    margin-top: -6em;
}

.games-area .container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1em;
    transform: translateY(-4em);
    justify-content: space-between;
}

.games-area img {
    transition: all 300ms var(--cubic)
}

.games-area a:hover img {
    transform: scale(1.1)
}


/* Promation Area */

.promotion-area {
    text-align: center;
    color: #fff;
    background-image: url('../img/promobg.png');
    background-position: top center;
    background-repeat: no-repeat;
    background-color: #161b2b;
    padding: 6em 0
}

.promotion-area h2 {
    font-size: 2em;
    margin: 0 0 .5em 0
}

.promotion-area p {
    max-width: 70%;
    margin: 0 auto;
    font-size: 1.1em;
}


/* Promation Grid */

.promo-grid {
    margin-top: 4em;
    display: grid;
    grid-template-areas: "a a b c" "a a d e ";
    gap: 2em;
    text-align: left;
}

.promo-grid a {
    position: relative;
    display: inline-grid;
    grid-template-columns: 1fr auto;
    align-items: flex-start;
    gap: 1em;
    padding: 2em;
    background-color: rgba(255, 255, 255, 0.1);
    background-image: url('../img/gridbg.png');
    background-position: right top;
    background-repeat: no-repeat;
    transition: all 200ms var(--cubic)
}

.promo-grid a:hover {
    transform: scale(1.02)
}

.promo-grid .info {
    position: relative;
    z-index: 22;
}

.promo-grid .button {
    position: absolute;
    bottom: -1em;
    left: -1em
}

.promo-grid h3,
.promo-grid p {
    margin: 0
}

.promo-grid h3 {
    font-weight: 400;
    color: var(--orange)
}

.promo-grid p {
    margin-top: 1em;
    font-size: .75em;
}

.promo-grid a:first-child {
    background-color: var(--orange);
    background-image: url('../img/gridbg1.png');
    grid-area: a;
    grid-template-columns: 1fr;
}

.promo-grid a:first-child h3 {
    color: #fff;
    font-size: 2.25em;
    font-weight: 700;
}

.promo-grid a:first-child p {
    color: #000;
    font-size: .875em;
}

.promo-grid a:not(:first-child) .grid-image {
    order: 1
}

.promo-grid a:not(:first-child) .grid-image img {
    max-width: 120px;
}


/* Footer */

.footer-top {
    background: #121623;
}

.footer-top .container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 2em 0
}

.footer-cizgi {
    border-top: 1px solid #FDC730;
    opacity: .2;
}

.footer-logo {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    background: linear-gradient(to bottom, #121623 70%, #121623 70%, #151a28 70%, #151a28 100%);
}

.footer-logo img {
    position: relative;
    z-index: 2;
}

.footer-logo::after {
    content: "";
    position: absolute;
    top: 70%;
    width: 100%;
    height: 4px;
    background: var(--orange);
    z-index: 1;
}

.footer-bottom {
    color: #999;
    text-align: center;
    padding: 4em 0;
    background-color: #151a28;
    background-image: url('../img/footer-icon.png'), url('../img/footer-icon.png');
    background-position: left, right;
    background-repeat: no-repeat;
}

.social {
    margin-top: 2em;
    display: grid;
    grid-template-columns: repeat(5, auto);
    gap: 1em;
    justify-content: center;
}

.just-mobile {
    display: none;
}

.just-mobile .social {
    margin: 0;
    line-height: 1;
}

.mobile-show {
    display: none;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding: 1em;
    text-align: center;
    margin: 1em;
    background: #1c1f2c;
    color: var(--orange);
    font-weight: 700;
    text-transform: uppercase;
    clip-path: polygon(0 0, 100% 0, 95% 100%, 5% 100%);
}

.mobile-show svg {
    width: 1.5em;
    margin-left: 1em
}

.mobile-social {
    display: none;
}

@media screen and (min-width:1336px) {
    .container {
        max-width: 1200px;
    }
}

@media screen and (max-width:768px) {
    .just-mobile {
        display: unset;
    }
    .mobile-show {
        display: flex;
    }
    .header-text {
        margin-top: 0
    }
    .mobile-social {
        display: grid;
        grid-template-columns: repeat(5, auto);
        gap: 0;
        justify-content: center;
        gap: 1em;
        padding: .5em 1em;
        line-height: 1;
        background: rgb(28 31 44 / 0.6);
        backdrop-filter: blur(5px);
    }
    .mobile-social img {
        width: 48px;
    }
    .logoback {
        width: 100%;
        bottom: unset;
        height: 100%;
        top: 0;
    }
    .logo {
        transform: none;
        pointer-events: none;
    }
    .second-area {
        margin-top: 10em
    }
    .games-area {
        text-align: center;
    }
    .header-text .container {
        flex-direction: column;
    }
    .header ul {
        right: unset;
        top: -5em
    }
    .header .container {
        flex-direction: column;
    }
    .header-text h1::after {
        display: none;
    }
    .header-text h1 {
        text-align: center;
        padding: 0 1em;
        margin-bottom: .5em;
        font-weight: 700;
        line-height: 1;
        text-shadow: 0px 0px 5px #1c1f2c;
        font-size: 3em;
    }
    .header ul li {
        transform: none
    }
    .header ul li a {
        display: inline-grid;
        transform: none
    }
    .header-text p {
        text-align: center;
        padding: 0 2em;
		font-size:1.2em;
		color: #fff;
    text-shadow: 0 0 5px #1c1f2c;
    }
    .games-area .container {
        grid-template-columns: 1fr;
    }
    .promo-grid {
        grid-template-areas: "a";
        padding-left: 2em;
        padding-right: 2em
    }
    .games-area .container {
        transform: none;
        padding: 2em 0
    }
    .games-area {
        background-size: 100%;
        background-repeat: repeat-y;
    }
    .footer span {
        padding: 2em;
        text-align: center;
    }
    .footer img {
        max-width: 80%;
        margin-left: auto;
        margin-right: auto;
    }
    .header-text .container>* {
        max-width: 100%;
    }
}
