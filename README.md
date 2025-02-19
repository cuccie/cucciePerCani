<!DOCTYPE html>

<html lang="it">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Cucceshop Artigianale</title>

    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap">

    <style>

        /* Stili CSS in stile falegnameria */

        body {

            font-family: 'Roboto', sans-serif;

            background-color: #f5f5dc; /* Beige chiaro */

            color: #4b3621; /* Marrone scuro */

            margin: 0;

            padding: 0;

        }



        header {

            background-color: #8b4513; /* Marrone legno */

            color: white;

            padding: 40px 20px;

            text-align: center;

            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);

        }



        header h1 {

            margin: 0;

            font-size: 3em;

            font-weight: bold;

            text-transform: uppercase;

        }



        header p {

            margin: 10px 0 0;

            font-size: 1.2em;

        }



        .product-container {

            display: flex;

            flex-wrap: wrap;

            justify-content: center;

            padding: 20px;

            gap: 20px;

        }



        .product {

            background-color: white;

            border: 2px solid #8b4513; /* Bordo marrone legno */

            border-radius: 10px;

            padding: 20px;

            width: 250px;

            text-align: center;

            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);

            transition: transform 0.3s ease, box-shadow 0.3s ease;

        }



        .product:hover {

            transform: translateY(-10px);

            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);

        }



        .product img {

            max-width: 100%;

            border-radius: 10px;

            margin-bottom: 15px;

        }



        .product h3 {

            margin: 15px 0 10px;

            font-size: 1.5em;

            color: #8b4513; /* Marrone legno */

        }



        .product p {

            color: #666;

            font-size: 1em;

            line-height: 1.5;

        }



        .product .price {

            font-size: 1.2em;

            color: #228b22; /* Verde scuro */

            font-weight: bold;

            margin: 10px 0;

        }



        .product button {

            background-color: #228b22; /* Verde scuro */

            color: white;

            border: none;

            padding: 12px 24px;

            border-radius: 6px;

            cursor: pointer;

            font-size: 1em;

            font-weight: bold;

            transition: background-color 0.3s ease;

        }



        .product button:hover {

            background-color: #1e7a1e; /* Verde più scuro */

        }



        .carrello {

            background-color: white;

            border: 2px solid #8b4513; /* Bordo marrone legno */

            border-radius: 10px;

            padding: 20px;

            margin: 20px auto;

            max-width: 600px;

            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);

        }



        .carrello h2 {

            color: #8b4513; /* Marrone legno */

            text-align: center;

            font-size: 1.8em;

            margin-bottom: 20px;

        }



        .carrello ul {

            list-style-type: none;

            padding: 0;

        }



        .carrello ul li {

            padding: 10px;

            border-bottom: 1px solid #8b4513; /* Bordo marrone legno */

            font-size: 1em;

            color: #4b3621; /* Marrone scuro */

        }



        .carrello ul li:last-child {

            border-bottom: none;

        }



        .carrello .totale {

            font-size: 1.2em;

            font-weight: bold;

            text-align: right;

            margin-top: 20px;

            color: #8b4513; /* Marrone legno */

        }



        .carrello .sconto {

            color: #228b22; /* Verde scuro */

            font-weight: bold;

            text-align: right;

            margin-top: 10px;

        }



        .pagamento {

            background-color: white;

            border: 2px solid #8b4513; /* Bordo marrone legno */

            border-radius: 10px;

            padding: 20px;

            margin: 20px auto;

            max-width: 600px;

            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);

            display: none; /* Nascondi inizialmente */

        }



        .pagamento h2 {

            color: #8b4513; /* Marrone legno */

            text-align: center;

            font-size: 1.8em;

            margin-bottom: 20px;

        }



        .pagamento label {

            display: block;

            margin: 10px 0 5px;

            font-weight: bold;

            color: #4b3621; /* Marrone scuro */

        }



        .pagamento input, .pagamento select {

            width: 100%;

            padding: 10px;

            margin-bottom: 15px;

            border: 2px solid #8b4513; /* Bordo marrone legno */

            border-radius: 6px;

            font-size: 1em;

            background-color: #f5f5dc; /* Beige chiaro */

            color: #4b3621; /* Marrone scuro */

        }



        .pagamento input:invalid {

            border-color: #ff0000; /* Rosso per errore */

        }



        .pagamento button {

            width: 100%;

            padding: 15px;

            background-color: #228b22; /* Verde scuro */

            color: white;

            border: none;

            border-radius: 6px;

            font-size: 1.2em;

            font-weight: bold;

            cursor: pointer;

            transition: background-color 0.3s ease;

        }



        .pagamento button:hover {

            background-color: #1e7a1e; /* Verde più scuro */

        }



        footer {

            background-color: #8b4513; /* Marrone legno */

            color: white;

            text-align: center;

            padding: 20px;

            margin-top: 40px;

        }



        footer p {

            margin: 0;

            font-size: 0.9em;

        }



        .error-message {

            color: #ff0000; /* Rosso per errore */

            font-size: 0.9em;

            margin-top: 5px;

            display: none;

        }

    </style>

</head>

<body>



    <!-- Header -->

    <header>

        <h1>Cucceshop Artigianale</h1>

        <p>Realizzate a mano dal nostro falegname con amore e cura.</p>

    </header>



    <!-- Product Section -->

    <div class="product-container">

        <!-- Cuccia 1 -->

        <div class="product">

            <img src="https://via.placeholder.com/200" alt="Cuccia Classica">

            <h3>Cuccia Classica</h3>

            <p>Una cuccia comoda e resistente, perfetta per ogni cane.</p>

            <p class="price">€50</p>

            <button onclick="aggiungiAlCarrello('Cuccia Classica', 50)">Aggiungi al Carrello</button>

        </div>



        <!-- Cuccia 2 -->

        <div class="product">

            <img src="https://via.placeholder.com/200" alt="Cuccia di Lusso">

            <h3>Cuccia di Lusso</h3>

            <p>Una cuccia elegante con materiali di alta qualità.</p>

            <p class="price">€120</p>

            <button onclick="aggiungiAlCarrello('Cuccia di Lusso', 120)">Aggiungi al Carrello</button>

        </div>



        <!-- Cuccia 3 -->

        <div class="product">

            <img src="https://via.placeholder.com/200" alt="Cuccia da Esterno">

            <h3>Cuccia da Esterno</h3>

            <p>Robusta e impermeabile, ideale per il giardino.</p>

            <p class="price">€80</p>

            <button onclick="aggiungiAlCarrello('Cuccia da Esterno', 80)">Aggiungi al Carrello</button>

        </div>

    </div>



    <!-- Carrello Section -->

    <div class="carrello">

        <h2>Carrello</h2>

        <ul id="listaCarrello"></ul>

        <div class="totale">

            Totale: <span id="totaleCarrello">€0.00</span>

            <br>

            <span id="messaggioSconto" class="sconto"></span>

        </div>

        <button onclick="mostraPagamento()">Vai al Pagamento</button>

    </div>



    <!-- Pagamento Section -->

    <div class="pagamento" id="sezionePagamento">

        <h2>Pagamento</h2>

        <label for="metodoPagamento">Seleziona un metodo di pagamento:</label>

        <select id="metodoPagamento" onchange="mostraDati

Pagamento()">

            <option value="carta">Carta di credito</option>

            <option value="paypal">PayPal</option>

            <option value="bonifico">Bonifico bancario</option>

        </select>

        

        <div id="carta" class="metodoPagamentoForm" style="display:none;">

            <label for="numeroCarta">Numero Carta:</label>

            <input type="text" id="numeroCarta" placeholder="Inserisci numero carta" required>

            <label for="scadenzaCarta">Data di Scadenza:</label>

            <input type="month" id="scadenzaCarta" required>

            <label for="cvv">CVV:</label>

            <input type="text" id="cvv" placeholder="Inserisci CVV" required>

        </div>



        <div id="paypal" class="metodoPagamentoForm" style="display:none;">

            <label for="emailPaypal">Email PayPal:</label>

            <input type="email" id="emailPaypal" placeholder="Inserisci la tua email PayPal" required>

        </div>



        <div id="bonifico" class="metodoPagamentoForm" style="display:none;">

            <label for="iban">IBAN:</label>

            <input type="text" id="iban" placeholder="Inserisci IBAN" required>

        </div>



        <button onclick="concludiAcquisto()">Concludi l'Acquisto</button>

    </div>



    <!-- Footer -->

    <footer>

        <p>&copy; 2025 Cucceshop Artigianale - Tutti i diritti riservati</p>

    </footer>



    <script>

        let carrello = [];



        // Funzione per aggiungere un prodotto al carrello

        function aggiungiAlCarrello(nome, prezzo) {

            carrello.push({ nome, prezzo });

            aggiornaCarrello();

        }



        // Funzione per aggiornare la visualizzazione del carrello

        function aggiornaCarrello() {

            const listaCarrello = document.getElementById('listaCarrello');

            const totaleCarrello = document.getElementById('totaleCarrello');

            const messaggioSconto = document.getElementById('messaggioSconto');



            // Rimuovi tutti gli elementi esistenti

            listaCarrello.innerHTML = '';

            let totale = 0;



            // Aggiungi i prodotti al carrello

            carrello.forEach(item => {

                const li = document.createElement('li');

                li.textContent = `${item.nome} - €${item.prezzo}`;

                listaCarrello.appendChild(li);

                totale += item.prezzo;

            });



            // Mostra il totale

            totaleCarrello.textContent = `€${totale.toFixed(2)}`;



            // Mostra il messaggio sconto se il totale è maggiore di 100€

            if (totale >= 100) {

                messaggioSconto.textContent = 'Hai diritto ad uno sconto del 10%!';

                totale *= 0.9; // Applica il 10% di sconto

                totaleCarrello.textContent = `€${totale.toFixed(2)}`;

            } else {

                messaggioSconto.textContent = '';

            }

        }



        // Funzione per mostrare la sezione di pagamento

        function mostraPagamento() {

            const pagamento = document.getElementById('sezionePagamento');

            pagamento.style.display = 'block';

        }



        // Funzione per mostrare i campi relativi al metodo di pagamento selezionato

        function mostraDatiPagamento() {

            const metodoPagamento = document.getElementById('metodoPagamento').value;

            const formCarta = document.getElementById('carta');

            const formPaypal = document.getElementById('paypal');

            const formBonifico = document.getElementById('bonifico');



            formCarta.style.display = 'none';

            formPaypal.style.display = 'none';

            formBonifico.style.display = 'none';



            if (metodoPagamento === 'carta') {

                formCarta.style.display = 'block';

            } else if (metodoPagamento === 'paypal') {

                formPaypal.style.display = 'block';

            } else if (metodoPagamento === 'bonifico') {

                formBonifico.style.display = 'block';

            }

        }



        // Funzione per concludere l'acquisto

        function concludiAcquisto() {

            alert('Acquisto completato con successo! Grazie per aver scelto Cucceshop Artigianale.');

            // Resetta il carrello

            carrello = [];

            aggiornaCarrello();

            document.getElementById('sezionePagamento').style.display = 'none'; // Nascondi la sezione di pagamento

        }

    </script>

</body>

</html>
