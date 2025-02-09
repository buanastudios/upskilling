
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Accordion</title>
    <style>
        .accordion {
            display: flex;
            flex-direction: column;
            width: 100%;
            max-width: 600px;
        }
        .accordion-item {
            border-bottom: 1px solid #ccc;
        }
        .accordion-item input {
            display: none;
        }
        .tab-title {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px;
            cursor: pointer;
            background: #f9f9f9;
        }
        .tab-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
        }
        .accordion-item input:checked + .tab-title + .tab-content {
            max-height: 300px;
            padding: 10px;
        }
        .accordion-item input:checked + .tab-title .svg-icon {
            transform: rotate(90deg);
        }
        .svg-icon {
            transition: transform 0.3s ease;
        }
    </style>
</head>
<body>
    <div class="accordion">
        <div class="accordion-item">
            <input type="checkbox" id="tab1">
            <label class="tab-title" for="tab1">
                <span>Materi 1</span>
                <svg class="svg-icon" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M8 5L16 12L8 19" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </label>
            <div class="tab-content">
                <p>Konten Materi 1</p>
            </div>
        </div>

        <div class="accordion-item">
            <input type="checkbox" id="tab2">
            <label class="tab-title" for="tab2">
                <span>Materi 2</span>
                <svg class="svg-icon" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M8 5L16 12L8 19" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </label>
            <div class="tab-content">
                <p>Konten Materi 2</p>
            </div>
        </div>
    </div>
</body>
</html>
