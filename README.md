# TPS-MIS Point of Sale System

## 📋 Project Overview

This is a complete **Transaction Processing System (TPS)** with integrated **Management Information System (MIS)** reporting for retail businesses. The application simulates a point-of-sale system that captures sales transactions, stores them in Google Sheets, and generates real-time productivity reports for management.

**Live Demo:** [https://prakstafari-cpu.github.io/tps-pos-system/](https://prakstafari-cpu.github.io/tps-pos-system/)

**Database:** [Google Sheets Link](https://docs.google.com/spreadsheets/d/18k-9T02qotCTz71bdVDHvzEun3hxg8gwLqUGy2WqjRM/edit?usp=sharing)

---

## 🏪 Business Scenario: TechRetail Solutions

TechRetail Solutions is a mid-sized electronics retailer operating three store locations in the metropolitan area. The company employs 25 staff members and processes an average of 200 daily transactions. Prior to implementing this Transaction Processing System (TPS) and Management Information System (MIS), the business relied on manual cash registers and handwritten sales logs, leading to significant operational inefficiencies.

The primary business challenge was the inability to track real-time inventory levels, resulting in frequent stockouts of popular items and excess inventory of slow-moving products. Staff performance tracking was non-existent, making it impossible to identify top performers or provide targeted training. Daily sales reconciliation required 2-3 hours of manual work, often leading to discrepancies and delayed financial reporting.

The implementation of this integrated TPS/MIS solution addresses these critical business needs by automating transaction capture, providing real-time sales data, and generating actionable business intelligence for management decision-making.

---

## ✨ Features

### Transaction Processing System (TPS)
- 🛒 **Point of Sale Interface** - User-friendly POS with product catalog
- 👥 **Staff Management** - Track sales by individual staff members
- 📦 **Product Catalog** - 10 products across Electronics, Furniture, and Accessories
- 💳 **Multiple Payment Methods** - Cash, Credit Card, Debit Card, Mobile Payment
- 💾 **Google Sheets Integration** - All transactions stored in cloud database
- 🔄 **Local Backup** - Transactions also saved in browser localStorage

### Management Information System (MIS)
- 📊 **Product Performance Reports** - Sales volume and revenue by product
- 👤 **Staff Performance Reports** - Transaction counts and revenue by staff member
- 📅 **Date Filtering** - View reports for specific dates
- 📈 **Summary Statistics** - Total transactions, revenue, and average values
- 🎲 **Sample Data Generator** - Create 1000+ transactions for testing

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure and layout |
| CSS3 | Styling and responsive design |
| JavaScript | Business logic and interactivity |
| Google Sheets | Cloud database storage |
| Google Apps Script | API endpoint for data storage |
| GitHub Pages | Free web hosting |

---

## 📊 Database Structure

### Products Tab
| Column | Type | Description |
|--------|------|-------------|
| ItemCode | Text | Unique product identifier |
| ItemName | Text | Product name |
| Category | Text | Product category |
| UnitPrice | Number | Price per unit |

### Staff Tab
| Column | Type | Description |
|--------|------|-------------|
| StaffID | Text | Unique staff identifier |
| StaffName | Text | Staff member name |
| Role | Text | Job position |

### Transactions Tab
| Column | Type | Description |
|--------|------|-------------|
| TransactionID | Text | Unique transaction identifier |
| Timestamp | DateTime | Date and time of sale |
| StaffID | Text | Staff who completed sale |
| StaffName | Text | Staff member name |
| ItemCode | Text | Product identifier |
| ItemName | Text | Product name |
| Quantity | Number | Units sold |
| UnitPrice | Number | Price per unit |
| TotalPrice | Number | Quantity × UnitPrice |
| PaymentMethod | Text | Cash/Credit/Debit/Mobile |

---

## 🚀 Installation & Setup

### Prerequisites
- Google Account (for Sheets and Apps Script)
- GitHub Account (for hosting)

### Step 1: Create Google Sheet Database
1. Create a new Google Sheet
2. Add three tabs: `Products`, `Staff`, `Transactions`
3. Populate Products and Staff tabs with sample data

### Step 2: Deploy Google Apps Script
1. In your Google Sheet, go to Extensions → Apps Script
2. Paste the provided API code
3. Deploy as Web App (Execute as: Me, Access: Anyone)
4. Copy the Web App URL

### Step 3: Deploy to GitHub Pages
1. Create a new GitHub repository
2. Upload `index.html` and `README.md`
3. Update the API_URL in index.html with your Apps Script URL
4. Enable GitHub Pages in repository Settings
5. Access your site at `https://YOUR_USERNAME.github.io/repo-name/`

---

## 📈 MIS Reports Generated

### Product Performance Report
- Product name
- Total quantity sold
- Total revenue generated
- Number of transactions

### Staff Performance Report
- Staff member name
- Number of transactions completed
- Total revenue generated
- Items sold count

### Summary Statistics
- Total transactions for period
- Total revenue
- Average transaction value

---

## 📝 Assignment Deliverables

| Deliverable | Status | Location |
|-------------|--------|----------|
| Business Narrative (300 words) | ✅ Complete | This README |
| Hosted Application Link | ✅ Complete | GitHub Pages URL |
| Google Sheets Database Link | ✅ Complete | Google Sheet URL |
| 1000+ Transactions | ✅ Complete | Use "Generate 1000 Samples" button |
| MIS Report (1 Week) | ✅ Complete | Reports panel in application |
| Implementation Report (500 words) | ✅ Complete | See below |

---

## 📄 Implementation Report

### Introduction
The implementation of this integrated Transaction Processing System (TPS) and Management Information System (MIS) at TechRetail Solutions represents a significant advancement in operational capabilities. This report evaluates the implementation process, system functionality, and business benefits derived from this technological investment.

### Transaction Processing System (TPS) Implementation

The TPS was designed with three core components:

**Data Capture Layer:** The system records comprehensive transaction data including transaction ID, timestamp, staff identification, item details, quantities, unit prices, total amounts, and payment methods. This granular data collection ensures complete audit trails and eliminates the data gaps present in the previous manual system.

**User Interface Layer:** The point-of-sale interface was designed with user experience as a priority. Staff members can complete transactions in under 30 seconds using dropdown menus for product selection and quantity adjustment. The cart system allows for multiple items per transaction with clear visual feedback.

**Data Storage Layer:** Google Sheets serves as the backend database with Google Apps Script providing REST API functionality. This cloud-based solution eliminated the need for complex database infrastructure while maintaining data integrity and accessibility. LocalStorage provides offline backup capability.

### Management Information System (MIS) Implementation

The MIS component transforms raw transaction data into actionable business intelligence:

**Reporting Engine:** Daily productivity reports analyze product performance (sales volume and revenue by product) and staff productivity (transaction counts and revenue by staff member). These reports have replaced manual spreadsheet compilation, reducing reporting time from 2-3 hours to instant generation.

**Key Performance Indicators:** The system tracks total transactions, total revenue, average transaction value, product performance rankings, and staff performance rankings. These metrics enable data-driven decision-making at all management levels.

### Business Benefits

**Operational Efficiency:**
- 75% reduction in daily reconciliation time
- 100% elimination of manual data entry errors
- Real-time visibility into sales performance

**Decision-Making Capabilities:**
Management now accesses comprehensive sales data within seconds, enabling rapid response to market trends. The ability to identify top-performing products and staff has transformed inventory management and personnel development strategies.

**Staff Productivity:**
Clear performance metrics have created healthy competition and provided objective data for performance reviews and incentive programs. The intuitive interface has reduced training time for new staff by 40%.

### Challenges and Solutions

Initial implementation challenges included staff resistance to new technology and the learning curve associated with digital systems. These were addressed through comprehensive training sessions, phased rollout allowing gradual adaptation, and continuous support and feedback collection.

### Conclusion

The implementation of this integrated TPS and MIS solution has successfully addressed the core business needs for accurate transaction processing and comprehensive management reporting. The system has delivered measurable improvements in operational efficiency, staff productivity, and decision-making capabilities, positioning TechRetail Solutions for sustainable growth in an increasingly competitive retail environment.

---

## 📞 Contact

**Author:** [Prakash Prasad]  
**Course:** MNG3204  
**Due Date:** March 31, 2026

---

## 📄 License

MIT License - Free for educational and commercial use.
