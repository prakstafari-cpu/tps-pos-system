<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prasad's IT Essentials - TPS MIS System Documentation</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #f0f2f5;
            padding: 40px 20px;
            color: #1a2a3a;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 24px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 32px;
            margin-bottom: 10px;
        }

        .header p {
            opacity: 0.9;
            font-size: 18px;
        }

        /* Content */
        .content {
            padding: 40px;
        }

        /* Section Styles */
        .section {
            margin-bottom: 40px;
            border-bottom: 1px solid #e0e0e0;
            padding-bottom: 30px;
        }

        .section:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .section h2 {
            color: #1e3c72;
            font-size: 24px;
            margin-bottom: 20px;
            padding-left: 12px;
            border-left: 4px solid #2a5298;
        }

        .section h3 {
            color: #2a5298;
            font-size: 18px;
            margin: 20px 0 12px 0;
        }

        /* Links Box */
        .links-box {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            background: #f8f9fa;
            border-radius: 16px;
            padding: 20px;
            margin-bottom: 20px;
        }

        .link-card {
            flex: 1;
            min-width: 250px;
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
            border: 1px solid #e0e0e0;
            transition: transform 0.2s;
        }

        .link-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .link-card h3 {
            margin-top: 0;
            color: #1e3c72;
            font-size: 16px;
            margin-bottom: 12px;
        }

        .link-card a {
            color: #2a5298;
            text-decoration: none;
            word-break: break-all;
            font-size: 14px;
        }

        .link-card a:hover {
            text-decoration: underline;
        }

        /* Tables */
        .data-table {
            width: 100%;
            border-collapse: collapse;
            margin: 15px 0;
            font-size: 14px;
            overflow-x: auto;
            display: block;
        }

        .data-table th,
        .data-table td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #e0e0e0;
        }

        .data-table th {
            background: #f8f9fa;
            color: #1e3c72;
            font-weight: 600;
        }

        .data-table tr:hover {
            background: #f8f9fa;
        }

        /* Feature Grid */
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 16px;
            margin: 20px 0;
        }

        .feature-card {
            background: #f8f9fa;
            border-radius: 12px;
            padding: 16px;
            border-left: 3px solid #2a5298;
        }

        .feature-card strong {
            color: #1e3c72;
            display: block;
            margin-bottom: 8px;
            font-size: 16px;
        }

        .feature-card p {
            color: #555;
            font-size: 14px;
            margin: 0;
        }

        /* Steps */
        .steps {
            counter-reset: step;
            list-style: none;
            padding: 0;
        }

        .steps li {
            counter-increment: step;
            margin-bottom: 20px;
            padding-left: 48px;
            position: relative;
        }

        .steps li::before {
            content: counter(step);
            background: #2a5298;
            color: white;
            width: 32px;
            height: 32px;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            position: absolute;
            left: 0;
            top: 0;
            font-weight: bold;
            font-size: 14px;
        }

        .sub-steps {
            margin-top: 10px;
            margin-left: 20px;
            list-style: none;
        }

        .sub-steps li {
            margin-bottom: 8px;
            padding-left: 24px;
            position: relative;
            counter-increment: none;
        }

        .sub-steps li::before {
            content: "•";
            background: none;
            color: #2a5298;
            width: auto;
            height: auto;
            font-size: 18px;
            top: -2px;
        }

        /* Badges */
        .badge {
            display: inline-block;
            background: #e8f0fe;
            color: #1e3c72;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 500;
            margin-right: 8px;
            margin-bottom: 8px;
        }

        /* Notes */
        .note-box {
            background: #e8f5e9;
            border-left: 4px solid #28a745;
            padding: 16px 20px;
            border-radius: 12px;
            margin-top: 20px;
        }

        .note-box p {
            margin: 0;
            color: #2e5c2e;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .content {
                padding: 20px;
            }
            .header {
                padding: 30px 20px;
            }
            .data-table {
                font-size: 12px;
            }
            .data-table th,
            .data-table td {
                padding: 8px;
            }
        }

        hr {
            margin: 20px 0;
            border: none;
            border-top: 1px solid #e0e0e0;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>🖥️ Prasad's IT Essentials</h1>
            <p>Transaction Processing System (TPS) & Management Information System (MIS)</p>
            <p style="font-size: 14px; margin-top: 10px;">Complete Documentation</p>
        </div>

        <!-- Content -->
        <div class="content">
            <!-- Project Links -->
            <div class="section">
                <h2>🔗 Project Links</h2>
                <div class="links-box">
                    <div class="link-card">
                        <h3>🌐 Hosted Application</h3>
                        <a href="https://prakstafari-cpu.github.io/tps-pos-system/" target="_blank">https://prakstafari-cpu.github.io/tps-pos-system/</a>
                    </div>
                    <div class="link-card">
                        <h3>📊 Google Sheets Database</h3>
                        <a href="https://docs.google.com/spreadsheets/d/18k-9T02qotCTz71bdVDHvzEun3hxg8gwLqUGy2WqjRM/edit?usp=sharing" target="_blank">View Transaction Database</a>
                    </div>
                </div>
            </div>

            <!-- Brief Description -->
            <div class="section">
                <h2>📖 Brief Description</h2>
                <p style="line-height: 1.6; color: #333;">Prasad's IT Essentials is a web-based <strong>Transaction Processing System (TPS)</strong> integrated with a <strong>Management Information System (MIS)</strong> designed for retail businesses. The application simulates a point-of-sale system that captures sales transactions including staff details, product information, quantities, prices, and payment methods. All transactions are stored in a Google Sheets database, and the system generates real-time daily productivity reports for management analysis. The application serves as a complete solution for processing sales, tracking inventory, and monitoring staff performance.</p>
            </div>

            <!-- Application Features -->
            <div class="section">
                <h2>✨ Application Features</h2>
                <div class="feature-grid">
                    <div class="feature-card"><strong>🛒 Point of Sale Interface</strong><p>User-friendly form with product selection, quantity controls, and price display</p></div>
                    <div class="feature-card"><strong>👥 Staff Selection</strong><p>Dropdown menu to assign transactions to specific staff members</p></div>
                    <div class="feature-card"><strong>📦 Product Catalog</strong><p>Complete product listing with categories and pricing</p></div>
                    <div class="feature-card"><strong>🔢 Quantity Controls</strong><p>+/- buttons for easy quantity adjustment</p></div>
                    <div class="feature-card"><strong>✅ Stock Validation</strong><p>Real-time inventory checking to prevent overselling</p></div>
                    <div class="feature-card"><strong>🛍️ Shopping Cart</strong><p>Multi-item cart with subtotal calculation and item removal</p></div>
                    <div class="feature-card"><strong>💳 Payment Methods</strong><p>Support for Cash, Credit Card, Debit Card, and Mobile Payment</p></div>
                    <div class="feature-card"><strong>☁️ Cloud Database</strong><p>All transactions saved to Google Sheets via API</p></div>
                    <div class="feature-card"><strong>💾 Local Backup</strong><p>Transactions stored in browser localStorage for redundancy</p></div>
                </div>
            </div>

            <!-- MIS -->
            <div class="section">
                <h2>📊 Management Information System (MIS)</h2>
                <p style="margin-bottom: 15px;">The MIS component provides comprehensive reporting capabilities for business management:</p>
                <div class="feature-grid">
                    <div class="feature-card"><strong>📈 Sales Report</strong><p>Total transactions, revenue, items sold, average transaction value, top selling products, payment method distribution</p></div>
                    <div class="feature-card"><strong>📂 Category Analysis</strong><p>Sales performance by product category including revenue, units sold, and average transaction value</p></div>
                    <div class="feature-card"><strong>📦 Inventory Status</strong><p>Real-time stock levels, out-of-stock alerts, reorder recommendations, total inventory value</p></div>
                    <div class="feature-card"><strong>👤 Staff Performance</strong><p>Individual staff metrics: transaction count, items sold, revenue generated, average transaction value</p></div>
                </div>
                <div style="background: #eef2fa; padding: 15px; border-radius: 12px; margin-top: 10px;">
                    <p style="margin: 0;"><strong>➕ Additional MIS Capabilities:</strong> Date filtering for specific date ranges • Last 7 days quick report • Performance rankings and recognition highlights • Low stock and critical inventory alerts</p>
                </div>
            </div>

            <!-- Technology Stack -->
            <div class="section">
                <h2>🛠️ Technology Stack</h2>
                <table class="data-table">
                    <thead>
                        <tr><th>Component</th><th>Technology</th><th>Purpose</th></tr>
                    </thead>
                    <tbody>
                        <tr><td><strong>Frontend</strong></td><td>HTML5, CSS3, JavaScript</td><td>User interface, business logic, client-side processing</td></tr>
                        <tr><td><strong>Backend API</strong></td><td>Google Apps Script</td><td>REST API endpoint for database operations</td></tr>
                        <tr><td><strong>Database</strong></td><td>Google Sheets</td><td>Cloud storage for products, staff, and transaction data</td></tr>
                        <tr><td><strong>Hosting</strong></td><td>GitHub Pages</td><td>Free web hosting for the application</td></tr>
                    </tbody>
                </table>
            </div>

            <!-- Database Structure -->
            <div class="section">
                <h2>📁 Database Structure</h2>
                
                <h3>📦 Products Tab</h3>
                <table class="data-table">
                    <thead><tr><th>Column</th><th>Data Type</th><th>Description</th></tr></thead>
                    <tbody>
                        <tr><td>ItemCode</td><td>Text</td><td>Unique product identifier</td></tr>
                        <tr><td>ItemName</td><td>Text</td><td>Product name</td></tr>
                        <tr><td>Category</td><td>Text</td><td>Product category (Electronics/Accessories/Storage)</td></tr>
                        <tr><td>UnitPrice</td><td>Number</td><td>Price per unit</td></tr>
                        <tr><td>StockQuantity</td><td>Number</td><td>Current inventory level</td></tr>
                        <tr><td>ReorderLevel</td><td>Number</td><td>Minimum stock threshold for alerts</td></tr>
                        <tr><td>ReorderQuantity</td><td>Number</td><td>Suggested order quantity</td></tr>
                    </tbody>
                </table>

                <h3>👥 Staff Tab</h3>
                <table class="data-table">
                    <thead><tr><th>Column</th><th>Data Type</th><th>Description</th></tr></thead>
                    <tbody>
                        <tr><td>StaffID</td><td>Text</td><td>Unique staff identifier</td></tr>
                        <tr><td>StaffName</td><td>Text</td><td>Staff member full name</td></tr>
                        <tr><td>Role</td><td>Text</td><td>Job position</td></tr>
                    </tbody>
                </table>

                <h3>📝 Transactions Tab</h3>
                <table class="data-table">
                    <thead><tr><th>Column</th><th>Data Type</th><th>Description</th></tr></thead>
                    <tbody>
                        <tr><td>TransactionID</td><td>Text</td><td>Unique transaction identifier</td></tr>
                        <tr><td>Timestamp</td><td>DateTime</td><td>Date and time of transaction</td></tr>
                        <tr><td>StaffID</td><td>Text</td><td>Staff who processed sale</td></tr>
                        <tr><td>StaffName</td><td>Text</td><td>Staff member name</td></tr>
                        <tr><td>ItemCode</td><td>Text</td><td>Product identifier</td></tr>
                        <tr><td>ItemName</td><td>Text</td><td>Product name</td></tr>
                        <tr><td>Category</td><td>Text</td><td>Product category</td></tr>
                        <tr><td>Quantity</td><td>Number</td><td>Units sold</td></tr>
                        <tr><td>UnitPrice</td><td>Number</td><td>Price per unit</td></tr>
                        <tr><td>TotalPrice</td><td>Number</td><td>Quantity × UnitPrice</td></tr>
                        <tr><td>PaymentMethod</td><td>Text</td><td>Cash/Credit Card/Debit Card/Mobile Payment</td></tr>
                    </tbody>
                </table>
            </div>

            <!-- How to Use -->
            <div class="section">
                <h2>🚀 How to Use the Application</h2>
                
                <h3>Step 1: Access the Application</h3>
                <p>Navigate to the hosted application URL and wait for the interface to load.</p>

                <h3>Step 2: Load Data from Google Sheets</h3>
                <p>Click the <strong>"Load from Google Sheets"</strong> button at the top of the reports section. This fetches the latest products, staff, and transaction data from the cloud database.</p>

                <h3>Step 3: Process a New Transaction</h3>
                <ul class="steps">
                    <li>Select a <strong>Staff Member</strong> from the dropdown list</li>
                    <li>Select a <strong>Product</strong> from the product dropdown</li>
                    <li>Review the <strong>Unit Price</strong> (auto-populated)</li>
                    <li>Check <strong>Current Stock</strong> to ensure availability</li>
                    <li>Enter <strong>Quantity</strong> using +/- buttons or type a number</li>
                    <li>Select <strong>Payment Method</strong> (Cash, Credit Card, Debit Card, Mobile Payment)</li>
                    <li>Click <strong>"Add to Cart"</strong> to include the item</li>
                    <li>Repeat steps 2-7 to add multiple items</li>
                    <li>Review the <strong>Cart</strong> and Subtotal</li>
                    <li>Click <strong>"Complete Sale"</strong> to finalize and save to database</li>
                </ul>

                <h3>Step 4: View MIS Reports</h3>
                <ul class="steps">
                    <li>Ensure data is loaded (click <strong>"Load from Google Sheets"</strong> if needed)</li>
                    <li>Select a date using the date picker or click <strong>"Last 7 Days"</strong></li>
                    <li>Click <strong>"Generate Report"</strong> to update all report tabs</li>
                    <li>Navigate between tabs to view different reports:
                        <ul class="sub-steps">
                            <li><strong>Sales Report:</strong> Overall sales metrics and product performance</li>
                            <li><strong>Category Analysis:</strong> Performance by product category</li>
                            <li><strong>Inventory Status:</strong> Current stock levels and reorder recommendations</li>
                            <li><strong>Staff Performance:</strong> Individual staff member metrics</li>
                        </ul>
                    </li>
                </ul>

                <h3>Step 5: Monitor Key Statistics</h3>
                <p>The top statistics bar displays real-time:</p>
                <ul class="sub-steps" style="margin-bottom: 20px;">
                    <li>Total Transactions</li>
                    <li>Total Revenue</li>
                    <li>Items Sold</li>
                    <li>Average Transaction Value</li>
                </ul>

                <div class="note-box">
                    <p><strong>📝 Notes:</strong></p>
                    <p>• All transactions are automatically saved to Google Sheets when "Complete Sale" is clicked</p>
                    <p>• The system validates stock levels before allowing a sale</p>
                    <p>• Inventory levels are automatically reduced after each transaction</p>
                    <p>• Low stock items are highlighted with visual alerts</p>
                    <p>• Reports can be generated for any date range using the date picker</p>
                </div>
            </div>

            <!-- Footer -->
            <hr>
            <div style="text-align: center; padding: 20px 0 10px; color: #6c757d; font-size: 13px;">
                <p>Prasad's IT Essentials | Transaction Processing System & Management Information System</p>
                <p>© 2026 | For educational purposes</p>
            </div>
        </div>
    </div>
</body>
</html>
