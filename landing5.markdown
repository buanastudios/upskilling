
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pure CSS Accordion</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }

        .accordion {
            width: 100%;
            max-width: 600px;
            margin: auto;
        }

        .accordion-item {
            border-bottom: 1px solid #ccc;
        }

        /* Hide default checkbox */
        .accordion-item input {
            display: none;
        }

        .tab-title {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px;
            background: #f4f4f4;
            cursor: pointer;
            font-weight: bold;
        }

        .accordion-icon {
            transition: transform 0.3s ease;
        }

        /* Hide content by default */
        .tab-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-in-out;
            background: #fff;
            padding: 0 15px;
        }

        /* When checked, show content */
        .accordion-item input:checked + .tab-title + .tab-content {
            max-height: 300px; /* Adjust as needed */
            padding: 15px;
        }

        /* Rotate icon when opened */
        .accordion-item input:checked + .tab-title .accordion-icon {
            transform: rotate(180deg);
        }

    </style>
</head>
<body>

<div class="accordion">
    <div class="accordion-item">
        <input type="checkbox" id="tab-1">
        <label class="tab-title" for="tab-1">
            <span>Materi 1: How To Be A Great Communicator</span>
            <span class="accordion-icon">▼</span>
        </label>
        <div class="tab-content">
            <ul>
                <li>Pengantar Komunikasi Efektif</li>
                <li>Indikator & Cara Berkomunikasi Efektif</li>
                <li>Kedalaman Pesan</li>
                <li>Prinsip Dasar Komunikasi Efektif</li>
                <li>Komunikasi Organisasi</li>
                <li>Fundamental Komunikasi Efektif</li>
            </ul>
        </div>
    </div>

    <div class="accordion-item">
        <input type="checkbox" id="tab-2">
        <label class="tab-title" for="tab-2">
            <span>Materi 2: Manager as Coach</span>
            <span class="accordion-icon">▼</span>
        </label>
        <div class="tab-content">
            <ul>
                <li>Apa Itu Coaching?</li>
                <li>Perbedaan Coaching dengan Metode Lain</li>
                <li>Urgensi Manajer Sebagai Coach</li>
                <li>Langkah dalam Proses Coaching</li>
                <li>Keterampilan Coaching yang Harus Dimiliki</li>
                <li>Tujuan Akhir Coaching</li>
            </ul>
        </div>
    </div>

    <div class="accordion-item">
        <input type="checkbox" id="tab-3">
        <label class="tab-title" for="tab-3">
            <span>Materi 3: Change Management</span>
            <span class="accordion-icon">▼</span>
        </label>
        <div class="tab-content">
            <ul>
                <li>Pengantar Change Management</li>
                <li>Studi Kasus Change Management</li>
                <li>8 Langkah Proses Change Management</li>
                <li>4 Fase Transisi Perubahan</li>
                <li>Langkah Kecil, Dampak Besar</li>
            </ul>
        </div>
    </div>

</div>

</body>
</html>
