head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Top Up WDP - Mobile Legends</title>
    <style>
        body {
            margin: 0;
            font-family: 'Poppins', sans-serif;
            background: #1f1f2e;
            color: #fff;
        }

        .container {
            padding: 20px;
            max-width: 800px;
            margin: auto;
        }

        .right {
            background: #2bgre;
            border-radius: 12px;
            padding: 20px;
        }

        h2 {
            font-size: 20px;
            margin-bottom: 15px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        input {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: none;
            background: #383850;
            color: white;
        }

        .products {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .product-card {
            flex: 1 1 30%;
            background: #383850;
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            position: relative;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out;
        }

        .product-card:hover {
            background-color: #444444;
        }

        .product-card.selected {
            background-color: #444444;
            border: 2px solid #fff;
        }

        .product-card .discount {
            position: absolute;
            top: 10px;
            right: 10px;
            background: red;
            font-size: 10px;
            padding: 3px 5px;
            border-radius: 5px;
        }

        .price {
            margin-top: 10px;
            font-weight: bold;
            color: #f0f0f0;
        }

        .payment-options {
            margin-top: 20px;
        }

        .payment-options h3 {
            font-size: 18px;
            margin-bottom: 10px;
        }

        .payment-methods {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .payment-method {
            flex: 0 0 auto;
            background: #383850;
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out;
            width: 120px;
        }

        .payment-method:hover {
            background-color: #444444;
        }

        .payment-method img {
            max-height: 40px;
            margin-bottom: 10px;
            max-width: 100%;
            height: auto;
        }

        .payment-method.qris img {
            max-height: 120px;
        }

        #qris-section {
            display: none;
            text-align: center;
            margin-top: 20px;
        }

        #qris-section img {
            max-width: 200px;
            border: 1px solid #ddd;
            border-radius: 8px;
        }

        #qris-section p {
            font-size: 14px;
            color: #aaa;
            margin-top: 10px;
        }

        #top-image {
            max-width: 100%;
            height: auto;
            margin-bottom: 20px;
            border-radius: 8px;
        }

        /* Style untuk input file */
        #upload-bukti {
            margin-top: 10px;
        }

        #upload-bukti label {
            display: block;
            margin-bottom: 5px;
            font-size: 14px;
            color: #ccc;
        }

        #upload-bukti input[type="file"] {
            width: 100%;
            padding: 5px;
            border-radius: 4px;
            border: 1px solid #555;
            background: #383850;
            color: white;
        }

        /* Style untuk tombol konfirmasi di bawah QRIS */
        #konfirmasi-qris {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: none;
            background: #4CAF50;
            color: white;
            <!-- margin-top: 10px; -->
            <!-- cursor: pointer; -->
        <!-- } -->

        <!-- #konfirmasi-qris:hover { -->
            <!-- background-color: #45a049; -->
        <!-- } -->
    </style>
</head>

<body>
    <div class="container">
        <img id="top-image" src="Proyek Baru 16 [740DF4F].png" alt="Banner Top Up">

        <div class="right">
            <h2>1. Pilih Nominal Top Up</h2>
            <div class="products">
 <div class="product-card" onclick="selectNominal(this)" data-amount="26686"
                    data-diamond="Weekly Diamond Pass (Misi Top Up 100)">
					<img src="WDP.png" alt="Diamond" />
                    <div>Weekly Diamond Pass<br>(Misi Top Up 100)</div>
                    <div class="price">Rp 26.800,-</div>
                </div>
<div class="product-card" onclick="selectNominal(this)" data-amount="26686"
                    data-diamond="Weekly Diamond Pass (Misi Top Up 100)">
					<img src="WDP.png" alt="Diamond" />
                    <div>2x Weekly Diamond Pass<br></div>
                    <div class="price">Rp 53.400,-</div>
                </div>
<div class="product-card" onclick="selectNominal(this)" data-amount="1466" data-diamond="5 Diamonds">
    <div class="discount">10% OFF</div>
    <img src="3.png" alt="Diamond" />
    <div>5 (+0) Diamonds</div>
    <div class="price">Rp 1.466,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="3000" data-diamond="10 Diamonds">
    <div class="discount"></div>
    <img src="3.png" alt="Diamond" />
    <div>10 (+0) Diamonds</div>
    <div class="price">Rp 3.000,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="3500" data-diamond="12 Diamonds">
    <div class="discount"></div>
    <img src="3.png" alt="Diamond" />
    <div>12 (+1) Diamonds</div>
    <div class="price">Rp 3.500,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="5500" data-diamond="19 Diamonds">
    <div class="discount"></div>
    <img src="3.png" alt="Diamond" />
    <div>19 (+2) Diamonds</div>
    <div class="price">Rp 5.500,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="8000" data-diamond="28 Diamonds">
    <div class="discount"></div>
    <img src="3.png" alt="Diamond" />
    <div>28 (+3) Diamonds</div>
    <div class="price">Rp 8.000,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="9500" data-diamond="33 Diamonds">
    <div class="discount"></div>
    <img src="3.png" alt="Diamond" />
    <div>33 (+3) Diamonds</div>
    <div class="price">Rp 9.500,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="12000" data-diamond="44 Diamonds">
    <div class="discount"></div>
    <img src="3.png" alt="Diamond" />
    <div>44 (+4) Diamonds</div>
    <div class="price">Rp 12.000,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="15666" data-diamond="59 Diamonds">
    <div class="discount"></div>
    <img src="5.png" alt="Diamond" />
    <div>59 (+6) Diamonds</div>
    <div class="price">Rp 15.666,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="19000" data-diamond="71 Diamonds">
    <div class="discount"></div>
    <img src="5.png" alt="Diamond" />
    <div>71 (+7) Diamonds</div>
    <div class="price">Rp 19.000,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="22500" data-diamond="85 Diamonds">
    <div class="discount">11% OFF</div>
    <img src="5.png" alt="Diamond" />
    <div>85 (+8) Diamonds</div>
    <div class="price">Rp 22.500,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="26000" data-diamond="97 Diamonds">
    <div class="discount"></div>
    <img src="5.png" alt="Diamond" />
    <div>97 (+9) Diamonds</div>
    <div class="price">Rp 26.000,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="30000" data-diamond="113 Diamonds">
    <div class="discount"></div>
    <img src="KARUNG.png" alt="Diamond" />
    <div>113 (+11) Diamonds</div>
    <div class="price">Rp 30.000,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="44900" data-diamond="170 Diamonds">
    <div class="discount"></div>
    <img src="mobile_legends_weekly.png" alt="Diamond" />
    <div>170 (+16) Diamonds</div>
    <div class="price">Rp 44.900,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="59900" data-diamond="219 Diamonds">
    <div class="discount"></div>
    <img src="mobile_legends_weekly.png" alt="Diamond" />
    <div>219 (+20) Diamonds</div>
    <div class="price">Rp 59.900,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="64900" data-diamond="240 Diamonds">
    <div class="discount"></div>
    <img src="mobile_legends_weekly.png" alt="Diamond" />
    <div>240 (+23) Diamonds</div>
    <div class="price">Rp 64.900,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="73900" data-diamond="284 Diamonds">
    <div class="discount"></div>
    <img src="mobile_legends_weekly.png" alt="Diamond" />
    <div>284 (+27) Diamonds</div>
    <div class="price">Rp 73.900,-</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="76900" data-diamond="296 Diamonds">
    <div class="discount"></div>
    <img src="mobile_legends_weekly.png" alt="Diamond" />
    <div>296 (+40) Diamonds</div>
    <div class="price">Rp 76.900,-</div>
</div>
</div>
<div class="product-card" onclick="selectNominal(this)" data-amount="76900" data-diamond="296 Diamonds">
    <div class="discount"></div>
    <img src="brangkas.png" alt="Diamond" />
    <div>500 (+40) Diamonds</div>
    <div class="price">Rp 76.900,-</div>
</div
            </div>

            <h2>2. Informasi Pelanggan</h2>
            <div class="form-group">
                <input type="text" id="userId" placeholder="USER ID">
            </div>
            <div class="form-group">
                <input type="text" id="serverId" placeholder="Server">
            </div>

            <div class="payment-options">
                <h3>3. Pilih Metode Pembayaran</h3>
                <div class="payment-methods">
                    <div class="payment-method qris" onclick="handlePaymentClick('qris')">
                        <img src="Gambar WhatsApp 2025-04-26 pukul 16.45.10_1939ed9e.jpg" alt="QRIS">
                        QRIS
                    </div>
                </div>
            </div>

            <div id="qris-section">
                <h3>SCAN LALU TRANFER SESUAI NOMINAL DI ATAS UNTUK MELANJUTKAN</h3>
                <img src="qr.png" alt="QRIS">
                <p>PASTIKAN ID DAN SERVER SIDAH BENAR !!!</p>
                <p>kalo item yang kamu cari gk ada langsung ke wa aja ya</p>
                <button id="konfirmasi-qris" onclick="konfirmasiPesanan()">Konfirmasi</button>
            </div>
        </div>
    </div>

    <script>
        let selectedNominal = null;
        let selectedDiamond = null;
        let buktiTransferURL = null;

        function selectNominal(element) {
            if (selectedNominal) {
                selectedNominal.classList.remove('selected');
            }
            element.classList.add('selected');
            selectedNominal = element;

            const amount = element.dataset.amount;
            selectedDiamond = element.dataset.diamond;
            console.log('Nominal yang dipilih:', amount);
            console.log('Diamond yang dipilih:', selectedDiamond);
        }

        function handlePaymentClick(paymentMethod) {
            if (paymentMethod === 'qris') {
                document.getElementById('qris-section').style.display = 'block';
            } else {
                document.getElementById('qris-section').style.display = 'none';
            }
        }

        document.getElementById('bukti-transfer').addEventListener('change', function(event) {
            const file = event.target.files[0];
            if (file) {
                buktiTransferURL = URL.createObjectURL(file);
                console.log('URL Bukti Transfer:', buktiTransferURL);
            }
        });

        function konfirmasiPesanan() {
            const userId = document.getElementById('userId').value;
            const serverId = document.getElementById('serverId').value;
            const nominal = selectedNominal ? selectedNominal.dataset.amount : 'Belum dipilih';
            const diamond = selectedDiamond ? selectedDiamond : 'Belum dipilih';

            let pesan = `ID: ${userId}\nServer: ${serverId}\nNominal: Rp ${nominal},-\nDiamond: ${diamond}\n`;

            if (buktiTransferURL) {
                pesan += `\n*langsung kirim bukti tf sekalian ma teks ini ya.*`;
            } else {
                pesan += `\n*langsung kirim bukti tf sekalian ma teks ini ya.*`;
            }
			     if (buktiTransferURL) {
                pesan += `\n*PRODUCT MLBB.*`;
            } else {
                pesan += `\n*PRODUCT MLBB.*`;
            }

            const nomorWhatsApp = "6282328581304";
            const tautanWhatsApp = `https://wa.me/${nomorWhatsApp}?text=${encodeURIComponent(pesan)}`;
            window.open(tautanWhatsApp, '_blank');
        }
    </script>

</body>

</html>
<div id="index-container" style="display: none;">
    </div>
