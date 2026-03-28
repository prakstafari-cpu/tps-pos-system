# Prasad's IT Essentials - TPS MIS System

---

## 🔗 Project Links

| Link | URL |
|------|-----|
| **Hosted Application** | [https://prakstafari-cpu.github.io/tps-pos-system/](https://prakstafari-cpu.github.io/tps-pos-system/) |
| **Google Sheets Database** | [https://docs.google.com/spreadsheets/d/18k-9T02qotCTz71bdVDHvzEun3hxg8gwLqUGy2WqjRM/edit?usp=sharing](https://docs.google.com/spreadsheets/d/18k-9T02qotCTz71bdVDHvzEun3hxg8gwLqUGy2WqjRM/edit?usp=sharing) |

---

## 📖 Brief Description

Prasad's IT Essentials is a web-based **Transaction Processing System (TPS)** integrated with a **Management Information System (MIS)** designed for retail businesses. The application simulates a point-of-sale system that captures sales transactions including staff details, product information, quantities, prices, and payment methods. All transactions are stored in a Google Sheets database, and the system generates real-time daily productivity reports for management analysis. The application serves as a complete solution for processing sales, tracking inventory, and monitoring staff performance.

---

## ✨ Application Features

| Feature | Description |
|---------|-------------|
| **Point of Sale Interface** | User-friendly form with product selection, quantity controls, and price display |
| **Staff Selection** | Dropdown menu to assign transactions to specific staff members |
| **Product Catalog** | Complete product listing with categories and pricing |
| **Quantity Controls** | +/- buttons for easy quantity adjustment |
| **Stock Validation** | Real-time inventory checking to prevent overselling |
| **Shopping Cart** | Multi-item cart with subtotal calculation and item removal |
| **Payment Methods** | Support for Cash, Credit Card, Debit Card, and Mobile Payment |
| **Cloud Database** | All transactions saved to Google Sheets via API |
| **Local Backup** | Transactions stored in browser localStorage for redundancy |

---

## 📊 Management Information System (MIS)

The MIS component provides comprehensive reporting capabilities for business management:

| Report Type | Data Provided |
|-------------|---------------|
| **Sales Report** | Total transactions, total revenue, items sold, average transaction value, top selling products, payment method distribution |
| **Category Analysis** | Sales performance by product category including revenue, units sold, and average transaction value |
| **Inventory Status** | Real-time stock levels, out-of-stock alerts, reorder recommendations based on reorder levels, total inventory value |
| **Staff Performance** | Individual staff metrics including transaction count, items sold, revenue generated, and average transaction value |

**Additional MIS Capabilities:**
- Date filtering for specific date ranges
- Last 7 days quick report
- Performance rankings and recognition highlights
- Low stock and critical inventory alerts

---

## 🛠️ Technology Stack

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Frontend** | HTML5, CSS3, JavaScript | User interface, business logic, client-side processing |
| **Backend API** | Google Apps Script | REST API endpoint for database operations |
| **Database** | Google Sheets | Cloud storage for products, staff, and transaction data |
| **Hosting** | GitHub Pages | Free web hosting for the application |

---

## 📁 Database Structure

### Products Tab

| Column | Data Type | Description |
|--------|-----------|-------------|
| ItemCode | Text | Unique product identifier |
| ItemName | Text | Product name |
| Category | Text | Product category (Electronics/Accessories/Storage) |
| UnitPrice | Number | Price per unit |
| StockQuantity | Number | Current inventory level |
| ReorderLevel | Number | Minimum stock threshold for alerts |
| ReorderQuantity | Number | Suggested order quantity |

---

### Staff Tab

| Column | Data Type | Description |
|--------|-----------|-------------|
| StaffID | Text | Unique staff identifier |
| StaffName | Text | Staff member full name |
| Role | Text | Job position |

---

### Transactions Tab

| Column | Data Type | Description |
|--------|-----------|-------------|
| TransactionID | Text | Unique transaction identifier |
| Timestamp | DateTime | Date and time of transaction |
| StaffID | Text | Staff who processed sale |
| StaffName | Text | Staff member name |
| ItemCode | Text | Product identifier |
| ItemName | Text | Product name |
| Category | Text | Product category |
| Quantity | Number | Units sold |
| UnitPrice | Number | Price per unit |
| TotalPrice | Number | Quantity × UnitPrice |
| PaymentMethod | Text | Cash/Credit Card/Debit Card/Mobile Payment |

---

## 🚀 How to Use the Application

### Step 1: Access the Application
Navigate to the hosted application URL and wait for the interface to load.

### Step 2: Load Data from Google Sheets
Click the **"Load from Google Sheets"** button at the top of the reports section. This fetches the latest products, staff, and transaction data from the cloud database.

### Step 3: Process a New Transaction

| Step | Action |
|------|--------|
| 1 | Select a **Staff Member** from the dropdown list |
| 2 | Select a **Product** from the product dropdown |
| 3 | Review the **Unit Price** (auto-populated) |
| 4 | Check **Current Stock** to ensure availability |
| 5 | Enter **Quantity** using +/- buttons or type a number |
| 6 | Select **Payment Method** (Cash, Credit Card, Debit Card, Mobile Payment) |
| 7 | Click **"Add to Cart"** to include the item |
| 8 | Repeat steps 2-7 to add multiple items |
| 9 | Review the **Cart** and Subtotal |
| 10 | Click **"Complete Sale"** to finalize and save to database |

### Step 4: View MIS Reports

| Step | Action |
|------|--------|
| 1 | Ensure data is loaded (click **"Load from Google Sheets"** if needed) |
| 2 | Select a date using the date picker or click **"Last 7 Days"** |
| 3 | Click **"Generate Report"** to update all report tabs |
| 4 | Navigate between tabs to view different reports: |
|    | - **Sales Report:** Overall sales metrics and product performance |
|    | - **Category Analysis:** Performance by product category |
|    | - **Inventory Status:** Current stock levels and reorder recommendations |
|    | - **Staff Performance:** Individual staff member metrics |

### Step 5: Monitor Key Statistics
The top statistics bar displays real-time:
- Total Transactions
- Total Revenue
- Items Sold
- Average Transaction Value

---

## 📝 Notes

- All transactions are automatically saved to Google Sheets when "Complete Sale" is clicked
- The system validates stock levels before allowing a sale
- Inventory levels are automatically reduced after each transaction
- Low stock items are highlighted with visual alerts
- Reports can be generated for any date range using the date picker

---

## 📄 License

MIT License - Free for educational and commercial use.
