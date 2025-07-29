
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fetal Growth Calculator - Hadlock EFW Percentiles</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.3.0/papaparse.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/3.9.1/chart.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            padding: 30px;
            text-align: center;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }

        .header p {
            font-size: 1.1em;
            opacity: 0.9;
        }

        .main-content {
            padding: 40px;
        }

        .upload-section {
            background: #f8f9ff;
            border: 2px dashed #4facfe;
            border-radius: 10px;
            padding: 40px;
            text-align: center;
            margin-bottom: 30px;
            transition: all 0.3s ease;
        }

        .upload-section:hover {
            border-color: #00f2fe;
            background: #f0f4ff;
        }

        .upload-section.dragover {
            border-color: #00f2fe;
            background: #e6f3ff;
            transform: scale(1.02);
        }

        .upload-icon {
            font-size: 3em;
            color: #4facfe;
            margin-bottom: 20px;
        }

        .file-input {
            display: none;
        }

        .upload-btn {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 25px;
            font-size: 1.1em;
            cursor: pointer;
            transition: all 0.3s ease;
            margin: 10px;
        }

        .upload-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(79, 172, 254, 0.3);
        }

        .info-section {
            background: #fff9e6;
            border-left: 4px solid #ffc107;
            padding: 20px;
            margin-bottom: 30px;
            border-radius: 5px;
        }

        .info-section h3 {
            color: #e67e22;
            margin-bottom: 15px;
        }

        .info-section ul {
            margin-left: 20px;
        }

        .info-section li {
            margin-bottom: 8px;
        }

        .disclaimer {
            background: #ffe6e6;
            border-left: 4px solid #dc3545;
            padding: 20px;
            margin-bottom: 30px;
            border-radius: 5px;
        }

        .disclaimer h3 {
            color: #dc3545;
            margin-bottom: 15px;
        }

        .progress-section {
            display: none;
            margin-bottom: 30px;
        }

        .progress-bar {
            width: 100%;
            height: 20px;
            background: #e9ecef;
            border-radius: 10px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #4facfe, #00f2fe);
            width: 0%;
            transition: width 0.3s ease;
        }

        .progress-text {
            text-align: center;
            margin-top: 10px;
            font-weight: bold;
        }

        .results-section {
            display: none;
            background: #e8f5e8;
            border-left: 4px solid #28a745;
            padding: 20px;
            border-radius: 5px;
            margin-bottom: 30px;
        }

        .results-section h3 {
            color: #28a745;
            margin-bottom: 15px;
        }

        .chart-container {
            width: 100%;
            height: 500px;
            margin: 20px 0;
            background: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .chart-buttons {
            text-align: center;
            margin: 15px 0;
        }

        .download-btn {
            background: linear-gradient(135deg, #28a745 0%, #20c997 100%);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 25px;
            font-size: 1.1em;
            cursor: pointer;
            transition: all 0.3s ease;
            margin: 0 10px;
        }

        .download-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(40, 167, 69, 0.3);
        }

        .error-section {
            display: none;
            background: #ffe6e6;
            border-left: 4px solid #dc3545;
            padding: 20px;
            border-radius: 5px;
            margin-bottom: 30px;
        }

        .error-section h3 {
            color: #dc3545;
            margin-bottom: 15px;
        }

        .preview-table {
            max-height: 300px;
            overflow-y: auto;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-top: 20px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        th {
            background: #f8f9fa;
            font-weight: bold;
            position: sticky;
            top: 0;
        }

        tr:hover {
            background: #f8f9fa;
        }

        .footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 20px;
        }

        @media (max-width: 768px) {
            .main-content {
                padding: 20px;
            }
            
            .header h1 {
                font-size: 2em;
            }
            
            .upload-section {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Fetal Growth Calculator</h1>
            <p>Hadlock EFW Percentile Calculator - Based on 1991 Sonographic Weight Standard</p>
        </div>

        <div class="main-content">
            <div class="info-section">
                <h3>📋 Input File Instructions</h3>
                <p>Download the Excel template and fill in the columns according to their names:</p>
                <ul>
                    <li><strong>Column A:</strong> GA_week (Gestational Age in whole weeks)</li>
                    <li><strong>Column B:</strong> GA_day (Additional days, 0-6)</li>
                    <li><strong>Column C:</strong> uEFW (Estimated Fetal Weight in grams)</li>
                </ul>
                
                <div style="text-align: center; margin-top: 20px;">
                    <button class="upload-btn" onclick="downloadTemplate()">📥 Download Excel Template</button>
                </div>
            </div>

            <div class="disclaimer">
                <h3>⚠️ Important Disclaimers</h3>
                <ul>
                    <li><strong>Medical Disclaimer:</strong> This tool is for educational purposes only and is not intended to replace professional medical advice, diagnosis, or treatment.</li>
                    <li><strong>Calculation Note:</strong> EFW percentile calculations may show slight variations compared to ultrasound equipment or Table 1 values due to certain inconsistencies in the original Hadlock paper. This calculator uses the regression equation from the study.</li>
                    <li><strong>Data Processing:</strong> Decimal EFW values are automatically rounded down (e.g., 3750.6 → 3750). Empty rows are automatically skipped.</li>
                </ul>
            </div>

            <div class="upload-section" id="uploadSection">
                <div class="upload-icon">📁</div>
                <h3>Select Your Excel/CSV File</h3>
                <p>Drag and drop your file here or click to browse</p>
                <input type="file" id="fileInput" class="file-input" accept=".xlsx,.xls,.csv">
                <button class="upload-btn" onclick="document.getElementById('fileInput').click()">Choose File</button>
            </div>

            <div class="progress-section" id="progressSection">
                <h3>Processing...</h3>
                <div class="progress-bar">
                    <div class="progress-fill" id="progressFill"></div>
                </div>
                <div class="progress-text" id="progressText">Initializing...</div>
            </div>

            <div class="error-section" id="errorSection">
                <h3>❌ Error</h3>
                <p id="errorMessage"></p>
            </div>

            <div class="results-section" id="resultsSection">
                <h3>✅ Processing Complete</h3>
                <p id="resultsMessage"></p>
                <div class="chart-buttons">
                    <button class="download-btn" id="downloadBtn">📊 Download Results (Excel)</button>
                    <button class="download-btn" id="downloadChartBtn">📈 Download Chart (JPG)</button>
                </div>
                <div class="chart-container">
                    <canvas id="growthChart"></canvas>
                </div>
                <div class="preview-table" id="previewTable"></div>
            </div>
        </div>

        <div class="footer">
            <p>Based on: Hadlock FP, Harrist RB, Martinez-Poyer J. In utero analysis of fetal growth: a sonographic weight standard. Radiology. 1991 Oct;181(1):129-33.</p>
            <p>Created by Or Narkis</p>
        </div>
    </div>

    <script>
        let processedData = null;
        let originalFileName = '';
        let growthChart = null;

        // Hadlock percentile data (from the original study)
        const hadlockData = {
            weeks: [10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40],
            percentiles: {
                3: [26, 34, 43, 55, 70, 88, 110, 136, 167, 205, 248, 299, 359, 426, 503, 589, 685, 791, 908, 1034, 1169, 1313, 1465, 1622, 1783, 1946, 2110, 2271, 2427, 2576, 2714],
                10: [29, 37, 48, 61, 77, 97, 121, 150, 185, 227, 275, 331, 398, 471, 556, 652, 758, 876, 1004, 1145, 1294, 1453, 1621, 1794, 1973, 2154, 2335, 2513, 2686, 2851, 3004],
                50: [35, 45, 58, 73, 93, 117, 146, 181, 223, 273, 331, 399, 478, 568, 670, 785, 913, 1055, 1210, 1379, 1559, 1751, 1953, 2162, 2377, 2595, 2813, 3028, 3236, 3435, 3619],
                90: [41, 53, 68, 85, 109, 137, 171, 212, 261, 319, 387, 467, 559, 665, 784, 918, 1068, 1234, 1416, 1613, 1824, 2049, 2285, 2530, 2781, 3036, 3291, 3543, 3786, 4019, 4234],
                97: [44, 56, 73, 91, 116, 146, 183, 226, 279, 341, 414, 499, 598, 710, 838, 981, 1141, 1319, 1513, 1724, 1949, 2189, 2441, 2703, 2971, 3244, 3516, 3785, 4045, 4294, 4524]
            }
        };

        // Drag and drop functionality
        const uploadSection = document.getElementById('uploadSection');
        const fileInput = document.getElementById('fileInput');

        uploadSection.addEventListener('dragover', (e) => {
            e.preventDefault();
            uploadSection.classList.add('dragover');
        });

        uploadSection.addEventListener('dragleave', () => {
            uploadSection.classList.remove('dragover');
        });

        uploadSection.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadSection.classList.remove('dragover');
            const files = e.dataTransfer.files;
            if (files.length > 0) {
                handleFile(files[0]);
            }
        });

        fileInput.addEventListener('change', (e) => {
            if (e.target.files.length > 0) {
                handleFile(e.target.files[0]);
            }
        });

        function showProgress(show = true) {
            document.getElementById('progressSection').style.display = show ? 'block' : 'none';
        }

        function updateProgress(percent, message) {
            document.getElementById('progressFill').style.width = percent + '%';
            document.getElementById('progressText').textContent = message;
        }

        function showError(message) {
            document.getElementById('errorSection').style.display = 'block';
            document.getElementById('errorMessage').textContent = message;
        }

        function hideError() {
            document.getElementById('errorSection').style.display = 'none';
        }

        function showResults(message, data) {
            document.getElementById('resultsSection').style.display = 'block';
            document.getElementById('resultsMessage').textContent = message;
            
            // Create and update chart
            createGrowthChart(data);
            
            // Create preview table
            if (data && data.length > 0) {
                createPreviewTable(data.slice(0, 10)); // Show first 10 rows
            }
        }

        function createPreviewTable(data) {
            const previewDiv = document.getElementById('previewTable');
            
            let html = '<h4>Preview (first 10 rows):</h4><table>';
            
            // Headers
            if (data[0]) {
                html += '<tr>';
                Object.keys(data[0]).forEach(key => {
                    html += `<th>${key}</th>`;
                });
                html += '</tr>';
            }
            
            // Data rows
            data.forEach(row => {
                html += '<tr>';
                Object.values(row).forEach(value => {
                    html += `<td>${value}</td>`;
                });
                html += '</tr>';
            });
            
            html += '</table>';
            previewDiv.innerHTML = html;
        }

        function createGrowthChart(data) {
            const ctx = document.getElementById('growthChart').getContext('2d');
            
            // Destroy existing chart if it exists
            if (growthChart) {
                growthChart.destroy();
            }
            
            // Prepare datasets for percentile lines
            const datasets = [
                {
                    label: '3rd percentile',
                    data: hadlockData.weeks.map((week, i) => ({x: week, y: hadlockData.percentiles[3][i]})),
                    borderColor: '#dc3545',
                    backgroundColor: 'transparent',
                    borderWidth: 2,
                    fill: false,
                    pointRadius: 0,
                    tension: 0.1
                },
                {
                    label: '10th percentile',
                    data: hadlockData.weeks.map((week, i) => ({x: week, y: hadlockData.percentiles[10][i]})),
                    borderColor: '#007bff',
                    backgroundColor: 'transparent',
                    borderWidth: 2,
                    fill: false,
                    pointRadius: 0,
                    tension: 0.1
                },
                {
                    label: '50th percentile',
                    data: hadlockData.weeks.map((week, i) => ({x: week, y: hadlockData.percentiles[50][i]})),
                    borderColor: '#28a745',
                    backgroundColor: 'transparent',
                    borderWidth: 2,
                    fill: false,
                    pointRadius: 0,
                    tension: 0.1
                },
                {
                    label: '90th percentile',
                    data: hadlockData.weeks.map((week, i) => ({x: week, y: hadlockData.percentiles[90][i]})),
                    borderColor: '#fd7e14',
                    backgroundColor: 'transparent',
                    borderWidth: 2,
                    fill: false,
                    pointRadius: 0,
                    tension: 0.1
                },
                {
                    label: '97th percentile',
                    data: hadlockData.weeks.map((week, i) => ({x: week, y: hadlockData.percentiles[97][i]})),
                    borderColor: '#6f42c1',
                    backgroundColor: 'transparent',
                    borderWidth: 2,
                    fill: false,
                    pointRadius: 0,
                    tension: 0.1
                }
            ];
            
            // Add patient measurements
            const validMeasurements = data.filter(row => 
                row['Gestational Age (weeks)'] && row['uEFW (grams)']
            ).map(row => ({
                x: row['Gestational Age (weeks)'],
                y: row['uEFW (grams)']
            }));
            
            if (validMeasurements.length > 0) {
                datasets.push({
                    label: 'Measurements',
                    data: validMeasurements,
                    borderColor: '#333333',
                    backgroundColor: '#333333',
                    borderWidth: 0,
                    fill: false,
                    pointRadius: 2,
                    pointHoverRadius: 4,
                    showLine: false,
                    pointStyle: 'circle'
                });
            }
            
            growthChart = new Chart(ctx, {
                type: 'line',
                data: { datasets },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        title: {
                            display: true,
                            text: 'Fetal Growth Chart - Hadlock EFW Percentiles',
                            font: { size: 16, weight: 'bold' }
                        },
                        legend: {
                            position: 'top',
                            labels: {
                                boxWidth: 20,
                                padding: 15
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    if (context.dataset.label === 'Measurements') {
                                        return `${context.parsed.x} weeks: ${context.parsed.y}g`;
                                    }
                                    return `${context.dataset.label}: ${context.parsed.y}g`;
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            type: 'linear',
                            title: {
                                display: true,
                                text: 'Gestational Age (weeks)',
                                font: { weight: 'bold' }
                            },
                            min: 14,
                            max: 42,
                            grid: {
                                color: '#e9ecef'
                            }
                        },
                        y: {
                            title: {
                                display: true,
                                text: 'Estimated Fetal Weight (grams)',
                                font: { weight: 'bold' }
                            },
                            min: 0,
                            max: 5000,
                            grid: {
                                color: '#e9ecef'
                            }
                        }
                    }
                }
            });
        }

        async function handleFile(file) {
            hideError();
            showProgress();
            originalFileName = file.name.split('.').slice(0, -1).join('.');
            
            updateProgress(10, 'Reading file...');
            
            try {
                let data;
                
                if (file.name.toLowerCase().endsWith('.csv')) {
                    data = await parseCSV(file);
                } else {
                    data = await parseExcel(file);
                }
                
                updateProgress(30, 'Validating data...');
                
                const validatedData = validateAndCleanData(data);
                
                updateProgress(60, 'Calculating percentiles...');
                
                const resultsData = calculatePercentiles(validatedData);
                
                updateProgress(90, 'Preparing results...');
                
                processedData = resultsData;
                
                updateProgress(100, 'Complete!');
                
                setTimeout(() => {
                    showProgress(false);
                    showResults(`Successfully processed ${resultsData.length} records.`, resultsData);
                }, 500);
                
            } catch (error) {
                showProgress(false);
                showError(error.message);
            }
        }

        function parseCSV(file) {
            return new Promise((resolve, reject) => {
                Papa.parse(file, {
                    header: false,
                    complete: (results) => {
                        if (results.errors.length > 0) {
                            reject(new Error('CSV parsing error: ' + results.errors[0].message));
                        } else {
                            resolve(results.data);
                        }
                    },
                    error: (error) => {
                        reject(new Error('Failed to parse CSV: ' + error.message));
                    }
                });
            });
        }

        function parseExcel(file) {
            return new Promise((resolve, reject) => {
                const reader = new FileReader();
                reader.onload = (e) => {
                    try {
                        const data = new Uint8Array(e.target.result);
                        const workbook = XLSX.read(data, { type: 'array' });
                        const sheetName = workbook.SheetNames[0];
                        const worksheet = workbook.Sheets[sheetName];
                        const jsonData = XLSX.utils.sheet_to_json(worksheet, { header: 1 });
                        resolve(jsonData);
                    } catch (error) {
                        reject(new Error('Failed to parse Excel file: ' + error.message));
                    }
                };
                reader.onerror = () => reject(new Error('Failed to read file'));
                reader.readAsArrayBuffer(file);
            });
        }

        function validateAndCleanData(rawData) {
            if (!rawData || rawData.length === 0) {
                throw new Error('File appears to be empty');
            }

            const cleanedData = [];
            
            // Skip header row if it exists
            const startRow = rawData[0] && (isNaN(parseFloat(rawData[0][0])) || rawData[0][0] === 'GA_week') ? 1 : 0;
            
            for (let i = startRow; i < rawData.length; i++) {
                const row = rawData[i];
                
                // Skip completely empty rows
                if (!row || row.length === 0 || row.every(cell => !cell || cell === '')) {
                    continue;
                }
                
                // Check if we have at least 3 columns
                if (row.length < 3) {
                    // Add row with missing data as invalid
                    cleanedData.push({
                        originalRow: i + 1,
                        weeks: row[0] || '',
                        days: row[1] || '',
                        efw: row[2] || '',
                        isValid: false
                    });
                    continue;
                }
                
                // Extract values
                const weeks = parseInt(row[0]) || 0;
                const days = parseInt(row[1]) || 0;
                const efw = Math.floor(parseFloat(row[2]) || 0); // Round down decimals
                
                const gestationalAge = weeks + (days / 7);
                
                // Check if data is valid
                const isValid = !isNaN(gestationalAge) && !isNaN(efw) && 
                               gestationalAge >= 10 && gestationalAge <= 42 && 
                               efw > 0 && days >= 0 && days <= 6 && 
                               row[0] !== '' && row[1] !== '' && row[2] !== '';
                
                cleanedData.push({
                    originalRow: i + 1,
                    gestationalAge: isValid ? Math.round(gestationalAge * 10) / 10 : null,
                    weeks: row[0] || '',
                    days: row[1] || '',
                    efw: row[2] || '',
                    isValid: isValid
                });
            }
            
            if (cleanedData.length === 0) {
                throw new Error('No data rows found. Please check your file format and ensure you have 3 columns: GA_week, GA_day, uEFW');
            }
            
            return cleanedData;
        }

        function calculatePercentiles(data) {
            return data.map(row => {
                if (!row.isValid) {
                    // Return row with original data but empty calculated fields
                    return {
                        'GA_week': row.weeks,
                        'GA_day': row.days,
                        'Gestational Age (weeks)': '',
                        'uEFW (grams)': row.efw,
                        'Hadlock Percentile (%)': '',
                        'SGA': '',
                        'LGA': ''
                    };
                }
                
                const percentile = calculateEFWPercentile(row.gestationalAge, row.efw);
                
                return {
                    'GA_week': row.weeks,
                    'GA_day': row.days,
                    'Gestational Age (weeks)': row.gestationalAge,
                    'uEFW (grams)': row.efw,
                    'Hadlock Percentile (%)': Math.round(percentile * 10) / 10,
                    'SGA': percentile < 10 ? 1 : 0,
                    'LGA': percentile > 90 ? 1 : 0
                };
            });
        }

        // Hadlock EFW Percentile Calculation (from index.js)
        function calculateEFWPercentile(gestationalWeeks, efw) {
            if (isNaN(efw) || efw <= 0) {
                return 0;
            }

            // Hadlock regression equation: Log n weight (g) = 0.578 + 0.332 MA - 0.00354 MA²
            const mean = Math.exp(0.578 + 0.332 * gestationalWeeks - 0.00354 * Math.pow(gestationalWeeks, 2));
            const sd = mean * 0.1323; // 1 standard deviation = ±12.7% ≈ 0.1323

            return normDist(efw, mean, sd, true) * 100;
        }

        function normDist(x, mean, sd, cumulative) {
            const z = (x - mean) / sd;
            if (cumulative) {
                return (1 + erf(z / Math.sqrt(2))) / 2;
            } else {
                return Math.exp(-0.5 * z * z) / (sd * Math.sqrt(2 * Math.PI));
            }
        }

        function erf(x) {
            // Approximation of error function
            const a1 = 0.254829592;
            const a2 = -0.284496736;
            const a3 = 1.421413741;
            const a4 = -1.453152027;
            const a5 = 1.061405429;
            const p = 0.3275911;

            const sign = x < 0 ? -1 : 1;
            x = Math.abs(x);

            const t = 1.0 / (1.0 + p * x);
            const y = 1.0 - (((((a5 * t + a4) * t) + a3) * t + a2) * t + a1) * t * Math.exp(-x * x);

            return sign * y;
        }

        // Download template functionality
        function downloadTemplate() {
            // Create template data with headers
            const templateData = [
                ['GA_week', 'GA_day', 'uEFW'],
                ['', '', ''],
                ['', '', ''],
                ['', '', ''],
                ['', '', ''],
                ['', '', ''],
                ['', '', ''],
                ['', '', ''],
                ['', '', ''],
                ['', '', '']
            ];
            
            const ws = XLSX.utils.aoa_to_sheet(templateData);
            
            // Style the header row
            const headerStyle = {
                fill: { fgColor: { rgb: "FFA500" } }, // Orange background
                font: { bold: true, color: { rgb: "FFFFFF" } }, // White text
                alignment: { horizontal: "center" }
            };
            
            // Apply styling to header cells
            ws['A1'].s = headerStyle;
            ws['B1'].s = headerStyle;
            ws['C1'].s = headerStyle;
            
            // Set column widths
            ws['!cols'] = [
                { wch: 12 }, // GA_week
                { wch: 12 }, // GA_day  
                { wch: 12 }  // uEFW
            ];
            
            const wb = XLSX.utils.book_new();
            XLSX.utils.book_append_sheet(wb, ws, 'Fetal_Growth_Template');
            
            XLSX.writeFile(wb, 'Fetal_Growth_Template.xlsx');
        }

        // Download functionality
        document.getElementById('downloadBtn').addEventListener('click', () => {
            if (!processedData) return;
            
            const ws = XLSX.utils.json_to_sheet(processedData);
            const wb = XLSX.utils.book_new();
            XLSX.utils.book_append_sheet(wb, ws, 'Results');
            
            const fileName = originalFileName + '_results.xlsx';
            XLSX.writeFile(wb, fileName);
        });

        // Download chart as JPG
        document.getElementById('downloadChartBtn').addEventListener('click', () => {
            if (!growthChart) return;
            
            // Create a temporary canvas with white background
            const canvas = document.getElementById('growthChart');
            const tempCanvas = document.createElement('canvas');
            const tempCtx = tempCanvas.getContext('2d');
            
            tempCanvas.width = canvas.width;
            tempCanvas.height = canvas.height;
            
            // Fill with white background
            tempCtx.fillStyle = 'white';
            tempCtx.fillRect(0, 0, tempCanvas.width, tempCanvas.height);
            
            // Draw the chart on top
            tempCtx.drawImage(canvas, 0, 0);
            
            // Create download link
            const link = document.createElement('a');
            link.download = (originalFileName || 'fetal_growth_chart') + '_chart.jpg';
            link.href = tempCanvas.toDataURL('image/jpeg', 0.9);
            link.click();
        });
    </script>
</body>
</html>
