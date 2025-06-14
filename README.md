# Inventory Management System

A Flask-based web application for managing inventory with comprehensive features for small to medium businesses.

## Features

- **Item Management**: Add, edit, update, and delete inventory items
- **Stock Tracking**: Monitor quantities, prices, and units
- **Expiry Management**: Track expiry dates and get alerts for items expiring soon
- **Low Stock Alerts**: Automatic notifications when stock falls below threshold (5 items)
- **Search Functionality**: Find items quickly by name
- **Sales Tracking**: Sell items with automatic quantity reduction
- **Inventory Reports**: Generate reports for low stock and expiring items
- **Total Value Calculation**: Real-time calculation of total inventory worth

## Technologies Used

- **Backend**: Python Flask
- **Database**: SQLite
- **Frontend**: HTML, CSS, Bootstrap 5
- **Template Engine**: Jinja2

## Project Structure

```
inventory-management-system/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── templates/            # HTML templates
│   ├── index.html        # Main dashboard
│   ├── edit.html         # Edit item page
│   └── report.html       # Reports page
├── inventory.db          # SQLite database (auto-created)
└── README.md            # This file
```

## Installation & Setup

### Local Development

1. **Clone or download the project files**

2. **Install Python dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**:
   ```bash
   python app.py
   ```

4. **Open your browser and go to**:
   ```
   http://localhost:5000
   ```

### Deployment Options

#### Render (Recommended)
1. Upload code to GitHub repository
2. Connect to Render.com
3. Create new Web Service
4. Settings:
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `python app.py`

#### Railway
1. Upload to GitHub
2. Connect to Railway.app
3. Deploy directly from repository

#### PythonAnywhere
1. Upload files to your account
2. Configure web app to point to `app.py`
3. Install dependencies in console

## Usage

### Adding Items
1. Fill in the "Add New Item" form on the main page
2. Required fields: Name, Quantity, Unit, Price
3. Optional: Expiry Date
4. Click "Add" to save

### Managing Stock
- **Edit**: Click "Edit" button next to any item
- **Delete**: Click "Delete" to remove item permanently
- **Sell**: Click "Sell" to reduce quantity by 1

### Monitoring
- **Low Stock**: Items with quantity < 5 are highlighted in yellow
- **Expiring Soon**: Items expiring within 7 days are highlighted in red
- **Search**: Use search bar to find specific items
- **Reports**: Click "View Report" for detailed low stock and expiry reports

## Database Schema

The SQLite database contains one main table:

```sql
CREATE TABLE items (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    quantity INTEGER NOT NULL,
    price REAL NOT NULL,
    expiry_date TEXT,
    unit TEXT
)
```

## Future Enhancements

- User authentication and authorization
- Category management
- Supplier tracking
- Purchase order management
- Barcode scanning
- Export to PDF/Excel
- Multi-location inventory
- Advanced reporting and analytics

## Author

Created as a 5th semester project demonstrating web development skills with Flask and database management.

## License

This project is open source and available under the MIT License.
