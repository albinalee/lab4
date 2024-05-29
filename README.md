<p align = "center">МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ<br>
РОССИЙСКОЙ ФЕДЕРАЦИИ<br>
ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ<br>
ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ<br>
«САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</p>
<br><br><br><br><br><br>
<p align = "center">Институт естественных наук и техносферной безопасности<br>Кафедра информатики<br>Ли Альбина Тевоновна</p>
<br><br><br>
<p align = "center"><br><strong>Лабораторная работа №4. «HTML»</strong><br>01.03.02 Прикладная математика и информатика</p>
<br><br><br><br><br><br><br><br><br><br><br><br>
<p align = "right">Научный руководитель<br>
Соболев Евгений Игоревич</p>
<br><br><br>
<p align = "center">г. Южно-Сахалинск<br>2024 г.</p>
<br><br><br><br><br><br><br><br><br><br><br><br>

<h1 align = "center">Введение</h1>

<p><b>Веб-разработка</b> — процесс создания веб-сайта или веб-приложения. Основными этапами процесса являются: </p>

<ul>
<li>Проектирование сайта или веб-приложения (сбор и анализ требований, разработка технического задания, проектирование интерфейсов);</li>
<li>Создание дизайн-концепции сайта;</li>
<li>Создание страниц;</li>
<li>Программирование;</li>
<li>Оптимизация и размещение материалов сайта;</li>
<li>Тестирование и внесение корректировок;</li>
<li>Публикация проекта на хостинге;</li>
<li>Обслуживание работающего сайта.</li>
</ul>

<br>

<h1 align = "center">Цели и задачи</h1>


<p>Цель: ознакомиться с принципами работы со стилями, классами.</p>

<p>Задачи:</p>

<ul>
<li>Создать несколько веб страниц</li>
<li>Научиться форматированию элементов при помощи стилей</li>
<li>Поэкспериментировать с классами, формами, кнопками, меню и т.д.</li>
</ul>

<p></p>

<h1 align = "center">Решение</h1>

<p>Для выполнения этой лабораторной работы, я пользовалась лекционным материалом и интернет-ресурсами для поиска решений задач оформления и для поиска медиаресурсов:</p>

<ul>
<li><a href="https://youtube.com/">YouTube</a></li>
<li><a href="https://stackoverflow.com/">Stack Overflow</a></li>
</ul>

<p>Создание меню:</p>
<code>.menu-btn {
    display: flex;
    width: 120px;
    height: 90px;
    justify-content: center;
    align-items: center;
}

.menu-btn span,
.menu-btn span:before,
.menu-btn span:after {
    content: '';
    display: block;
    height: 7px;
    width: 45px;
    border-radius: 7px;
    background-color: #ffffff;
    position: absolute;
}

.menu-btn span:before {
    bottom: 15px;
}

.menu-btn span:after {
    top: 15px;
}

.menu-btn:hover {
    opacity: 0.7;
    transition: all .5s;
}

#menu-btn-check:checked ~ .menu-btn span {
    background-color: rgba(255, 255, 255, 0);
    transition: all .5s;
}

#menu-btn-check:checked ~ .menu-btn span::before {
    bottom: 0;
    transform: rotate(45deg);
    transition: all .5s;
}

#menu-btn-check:checked ~ .menu-btn span::after {
    top: 0;
    transform: rotate(-45deg);
    transition: all .5s;
}

.menu-content {
    position: fixed;
    top: -200%;
    left: 0;
    z-index: 1;
    background: linear-gradient(to bottom, #b34513, #c54104);
    opacity: 0.9;
    width: 100%;
    height: 100vh;
    transition: all 0.5s;
}

.menu-btn-close {
    display: flex;
    width: 120px;
    height: 90px;
    margin-left: auto;
    margin-right: 1vh;
    justify-content: center;
    align-items: center;
}

.menu-btn-close span::before,
.menu-btn-close span::after {
    content: '';
    display: block;
    height: 7px;
    width: 45px;
    border-radius: 7px;
    background-color: #ffffff;
    position: absolute;
}

.menu-btn-close span::before {
    transform: rotate(45deg);
}

.menu-btn-close span::after {
    transform: rotate(-45deg);
}

.menu-btn-close:hover {
    opacity: 0.7;
    transition: all .5s;
}

#menu-btn-check:checked ~ .menu-content {
    top: 0;
}</code>
</br></br>
<p>Создание формы:</p>
<code>form {
    background: #808080;
    width: 300px;
    padding: 100px 100px;
    border-radius: 25px;
    margin: 0 auto;
    color: white;
}

label, input {
    display: block;
    font-size: 32px;
    line-height: 32px;
}

label {
    margin-bottom: 5px;
}

input {
    width: 280px;
    padding: 0 10px;
    border-radius: 10px;
    margin-bottom: 20px;
    outline: none;
}

form .btn {
    width: 250px;
    height: 75px;
    margin-top: 50px;
    font-size: 36px;
    line-height: 75px;
}</code>
</br></br>
<p>Создание анимации:</p>
<code>.carousel {
    display: flex;
    width: 700px;
    height: 400px;
    margin: 0 auto;
    overflow: hidden;
}

.carousel img {
    margin: 0;
    padding: 0;
    display: block;
}
@keyframes scroll {
    0% { margin-left: 0; }
    20% { margin-left: -100%; }
    30% { margin-left: -100%; }
    50% { margin-left: -200%; }
    60% { margin-left: -200%; }
    80% { margin-left: -300%; }
    90% { margin-left: -300%; }
    100% {margin-left: 0;}
}
.carousel > :first-child {
    animation-name: scroll;
    animation-duration: 20s;
    animation-delay: 0s;
    animation-iteration-count: infinite;
}</code>
</br></br>
<img src="/Images/ball.PNG"></img>
</br>
<code>@media(max-width: 767px) {
            header {
                height: 120px;
            }
            .header-title {
                font-size: 54px;
                line-height: 120px;
            }
            header .container div {
                display: none;
            }
            .return {
                width: 100px;
                height: 100px;
                border-radius: 50px;
            }
            p {
                text-indent: 40px;
                font-size: 28px;
                font-family: Calibri;
                text-align: justify;
            }
            span {
                font-size: 28px;
            }
            main {
                transform: scale(0.8, 0.8);
            }
        }
        p {
            text-indent: 40px;
            font-size: 32px;
            font-family: Calibri;
            text-align: justify;
        }
        body {
            background: linear-gradient(to bottom, #caac85, #4d4335);
        }
        .page-loader {
            position: absolute;
            top: -100vh;
            left: 0;
            z-index: 10;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(to top, #c5c56a, green);
            opacity: 0.9;
            width: 100vw;
            height: 100vh;
            animation: page-loader 3s 0s 1;
        }
        @keyframes page-loader {
            0% {
                top: 0;
            }
            66% {
                top: 0;
            }
            100% {
                top: -100vh;
            }
        }
        .page-loader h1 {
            opacity: 0;
            margin-top: 50px;
            color: rgb(183, 197, 141);
            text-shadow: black 5px 8px;
            font-size: 64px;
            letter-spacing: 1px;
            animation: fade-in 3.5s .5s 1;
        }
        @keyframes fade-in {
            20% {
                margin-top: 0;
                opacity: 1;
            }
            100% {
                margin-top: 0;
                opacity: 1;
            }</code>
</br></br>
<img src="/Images/pageloader.PNG"></img>
</br>
<h1 align = "center">Вывод</h1>
<p>В результате проделанной лабораторной работы, я познакомилась с новыми элементами языка html, потренировалась в написании стилей и более сложных структур разметки.</p>
