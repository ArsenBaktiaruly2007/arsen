<!DOCTYPE html>
<html lang="kk">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Емхана жазылу</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f4f8fb;
            color: #222;
        }

        header {
            background: #ffffff;
            padding: 20px 60px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
            color: #1687a7;
        }

        nav a {
            text-decoration: none;
            color: #333;
            margin-left: 25px;
            cursor: pointer;
        }

        nav a:hover {
            color: #1687a7;
        }

        .hero {
            background: #dff5fa;
            padding: 70px 60px;
            text-align: center;
        }

        .hero h1 {
            font-size: 40px;
            margin-bottom: 15px;
            color: #12677d;
        }

        .hero p {
            font-size: 18px;
            margin-bottom: 25px;
        }

        button {
            background: #1687a7;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            cursor: pointer;
        }

        button:hover {
            background: #12677d;
        }

        .container {
            max-width: 1100px;
            margin: 40px auto;
            padding: 0 20px;
        }

        h2 {
            text-align: center;
            margin-bottom: 25px;
            color: #12677d;
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 3px 12px rgba(0,0,0,0.08);
        }

        .card h3 {
            color: #1687a7;
            margin-bottom: 10px;
        }

        .form {
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 3px 12px rgba(0,0,0,0.08);
            max-width: 600px;
            margin: auto;
        }

        input,
        select {
            width: 100%;
            padding: 12px;
            margin: 8px 0 15px;
            border: 1px solid #ccc;
            border-radius: 7px;
        }

        .patient {
            background: white;
            padding: 15px;
            margin-bottom: 10px;
            border-radius: 8px;
            display: flex;
            justify-content: space-between;
        }

        footer {
            margin-top: 50px;
            background: #12677d;
            color: white;
            text-align: center;
            padding: 25px;
        }

        @media (max-width: 700px) {
            .cards {
                grid-template-columns: 1fr;
            }

            header {
                padding: 20px;
            }

            nav a {
                margin-left: 10px;
            }

            .hero {
                padding: 50px 20px;
            }
        }
    </style>
</head>

<body>

<header>

    <div class="logo">
        EMHANA
    </div>

    <nav>
        <a href="#home">Басты бет</a>
        <a href="#doctors">Дәрігерлер</a>
        <a href="#appointment">Жазылу</a>
        <a href="#patients">Пациенттер</a>
    </nav>

</header>


<section class="hero" id="home">

    <h1>Емханаға онлайн жазылу</h1>

    <p>
        Денсаулығыңызға қамқорлық жасау — біздің басты міндетіміз
    </p>

    <button onclick="scrollToAppointment()">
        Дәрігерге жазылу
    </button>

</section>


<section class="container" id="doctors">

    <h2>Дәрігерлер кестесі</h2>

    <div class="cards">

        <div class="card">

            <h3>Айдос Ермеков</h3>

            <p>Терапевт</p>

            <p>Дүйсенбі - Жұма</p>

            <p>09:00 - 14:00</p>

        </div>


        <div class="card">

            <h3>Аружан Сейтова</h3>

            <p>Кардиолог</p>

            <p>Дүйсенбі - Сенбі</p>

            <p>10:00 - 16:00</p>

        </div>


        <div class="card">

            <h3>Марат Қасымов</h3>

            <p>Стоматолог</p>

            <p>Сейсенбі - Жұма</p>

            <p>09:00 - 17:00</p>

        </div>

    </div>

</section>


<section class="container" id="appointment">

    <h2>Емханаға жазылу</h2>

    <div class="form">

        <label>Пациенттің аты-жөні:</label>

        <input
            type="text"
            id="patientName"
            placeholder="Аты-жөніңіз"
        >


        <label>Телефон:</label>

        <input
            type="tel"
            id="phone"
            placeholder="+7 700 000 00 00"
        >


        <label>Дәрігер:</label>

        <select id="doctor">

            <option value="">
                Дәрігерді таңдаңыз
            </option>

            <option value="Айдос Ермеков">
                Айдос Ермеков - Терапевт
            </option>

            <option value="Аружан Сейтова">
                Аружан Сейтова - Кардиолог
            </option>

            <option value="Марат Қасымов">
                Марат Қасымов - Стоматолог
            </option>

        </select>


        <label>Қабылдау күні:</label>

        <input
            type="date"
            id="date"
        >


        <label>Қабылдау уақыты:</label>

        <input
            type="time"
            id="time"
        >


        <button onclick="addPatient()">
            Жазылу
        </button>

    </div>

</section>


<section class="container" id="patients">

    <h2>Пациенттерді қабылдау</h2>

    <div id="patientList">

        <p>
            Әзірге пациенттер жоқ.
        </p>

    </div>

</section>


<footer>

    <p>© 2026 EMHANA</p>

    <p>Денсаулық — басты байлық</p>

</footer>


<script src="script.js"></script>

</body>

</html>
