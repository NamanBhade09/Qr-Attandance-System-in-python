# QR Code Attendance Management System ✅

A robust, production-ready real-time attendance tracking system built with Python. This system utilizes computer vision to scan QR codes, verify user identity, and log attendance automatically into a database with comprehensive reporting and analytics.

## 🌟 Key Features

### Core Functionality
- **📱 Real-Time QR Scanning** - High-speed QR code detection using OpenCV and PyZbar
- **⚡ Instant Logging** - Automatically records Name, ID, Date, Time, and Location
- **🚫 Duplicate Prevention** - Smart algorithm prevents multiple entries from the same user in a session
- **📊 Automatic CSV Reports** - Generates daily/weekly/monthly attendance sheets compatible with Excel
- **🔲 QR Code Generator** - Included utility to create custom QR codes for users
- **📈 Analytics Dashboard** - Visual attendance statistics, trends, and insights
- **🔐 Secure Access** - User authentication and role-based access control
- **📧 Automated Notifications** - Email alerts for absent members or pattern anomalies

### Advanced Features
- **Multi-Location Support** - Track attendance across different locations
- **Bulk Import/Export** - Import user lists, export attendance data
- **Customizable Rules** - Set attendance thresholds and alert conditions
- **Audit Trail** - Complete logging of all system activities
- **Export Formats** - CSV, Excel, PDF report generation
- **Real-Time Dashboard** - Live attendance monitoring

## 🛠️ Tech Stack

- **Language**: Python 3.7+
- **Computer Vision**: 
  - OpenCV - Image processing and QR code detection
  - PyZbar - QR code decoding
- **Data Processing**: 
  - Pandas - Data manipulation and analysis
  - NumPy - Numerical computing
- **QR Generation**: 
  - QRCode library - QR code creation
- **Database**: SQLite/MySQL
- **Web Interface** (Optional):
  - Flask - Web framework
  - SQLAlchemy - ORM
- **Export**: 
  - openpyxl - Excel file generation
  - reportlab - PDF generation

## 📋 Installation & Setup

### Prerequisites
```bash
- Python 3.7 or higher
- pip (Python package manager)
- Webcam for QR scanning
- SQLite or MySQL database
```

### Step-by-Step Installation

```bash
# 1. Clone the repository
git clone https://github.com/NamanBhade09/Qr-Attandance-System-in-python.git

# 2. Navigate to project directory
cd Qr-Attandance-System-in-python

# 3. Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 4. Install required packages
pip install -r requirements.txt

# 5. Configure settings
# Edit config.py with your database credentials and settings

# 6. Initialize database
python setup.py

# 7. Generate QR codes for users
python qr_generator.py

# 8. Run the application
python app.py
```

## 📁 Project Structure

```
Qr-Attendance-System-in-python/
├── app.py                 # Main application and entry point
├── scanner.py             # QR code scanning module using OpenCV
├── database.py            # Database configuration and models
├── qr_generator.py        # QR code generation script
├── reports.py             # Report generation module
├── config.py              # Configuration settings
├── requirements.txt       # Python dependencies
├── templates/             # HTML templates (if using web interface)
│   ├── dashboard.html
│   ├── reports.html
│   └── settings.html
├── static/                # CSS, JavaScript, images
│   ├── css/
│   ├── js/
│   └── images/
├── data/                  # Data storage
│   ├── users.csv
│   ├── attendance/
│   └── reports/
└── README.md             # Documentation
```

## 📝 Usage Guide

### For Administrators

1. **Generate QR Codes**
   ```bash
   python qr_generator.py
   # Creates unique QR codes for each user
   ```

2. **Monitor Attendance in Real-Time**
   - Open application dashboard
   - View live scan count
   - Monitor active sessions

3. **Generate Reports**
   ```bash
   python reports.py --date 2026-06-22 --format csv
   # Available formats: csv, excel, pdf
   ```

4. **Manage Users**
   - Add/remove users
   - Update user information
   - Assign locations

### For Users

1. **Scan QR Code**
   - Present QR code to camera
   - System validates and logs attendance
   - Receive confirmation message

2. **View Attendance History**
   - Access member portal
   - Check personal attendance records
   - Download reports

## 🔄 Workflow

```
1. Admin generates QR codes for users
   ↓
2. Users scan QR codes at check-in
   ↓
3. System validates QR code
   ↓
4. Duplicate prevention check
   ↓
5. Attendance recorded with timestamp
   ↓
6. Data saved to database
   ↓
7. Real-time dashboard updated
   ↓
8. Reports generated on demand
```

## 📊 Report Types

### Available Reports
- **Daily Attendance** - Complete attendance for a specific day
- **Weekly Summary** - Attendance trends and statistics
- **Monthly Report** - Comprehensive monthly analysis
- **Absent List** - Members absent on specific dates
- **Late Arrivals** - Members arriving after threshold time
- **Detailed History** - Complete attendance records per user
- **Custom Reports** - Filtered by date range, location, or user group

### Export Formats
- CSV (Excel compatible)
- Excel (.xlsx)
- PDF
- JSON

## 🔲 QR Code Generation

```bash
# Generate single QR code
python qr_generator.py --user_id USER001 --user_name "John Doe"

# Batch generate from CSV
python qr_generator.py --batch users.csv

# Save with custom output
python qr_generator.py --output ./qr_codes/ --size 300
```

## 🔐 Security Features

- User authentication with hashed passwords
- Role-based access control (Admin, Manager, User)
- Encrypted database credentials
- Session timeout protection
- Audit logs for all operations
- Input validation and sanitization
- Rate limiting on API endpoints

## ⚙️ Configuration

Edit `config.py` to customize:

```python
# Database settings
DB_TYPE = 'sqlite'  # or 'mysql'
DB_PATH = 'attendance.db'

# Scanner settings
CAMERA_ID = 0
RESOLUTION = (1280, 720)
FPS = 30

# Duplicate prevention (seconds)
DUPLICATE_INTERVAL = 5

# Report settings
REPORT_FORMAT = 'csv'
EXPORT_PATH = './reports/'

# Email notifications
ENABLE_EMAIL = True
SMTP_SERVER = 'smtp.gmail.com'
SENDER_EMAIL = 'your_email@gmail.com'
```

## 🤝 Contributing

Contributions are welcome and appreciated!

1. Fork the repository
2. Create feature branch (`git checkout -b feature/Enhancement`)
3. Make your improvements
4. Commit changes (`git commit -m 'Add Enhancement'`)
5. Push branch (`git push origin feature/Enhancement`)
6. Open a Pull Request with detailed description

## 📄 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

**Naman Bhade** - [GitHub Profile](https://github.com/NamanBhade09)

## 💡 Future Enhancements & Roadmap

- [ ] Mobile app (React Native/Flutter) for scanning
- [ ] Facial recognition integration for enhanced security
- [ ] Real-time SMS/Email notifications
- [ ] Multi-location support with branch management
- [ ] Advanced analytics dashboard with predictive insights
- [ ] Integration with existing ERP/HRMS systems
- [ ] Biometric authentication support
- [ ] Cloud storage and synchronization
- [ ] REST API for third-party integration
- [ ] Mobile app for attendance viewing

## 🐛 Troubleshooting

### QR Code Not Scanning
- **Solution**: Ensure camera permissions are enabled
- Check QR code quality and size (minimum 5cm x 5cm recommended)
- Verify QR generator is working correctly
- Try adjusting lighting conditions

### Database Connection Error
- **Solution**: Verify database credentials in `config.py`
- Ensure MySQL/SQLite service is running
- Check database name and user permissions
- Review connection string format

### Performance Issues
- **Solution**: Optimize database queries
- Add indexes to frequently searched columns
- Check system resources (CPU, RAM)
- Consider database cleanup for old records

### Camera Not Working
- **Solution**: Check camera is connected
- Verify camera permissions in system settings
- Try different camera ID in config
- Update camera drivers

## 📞 Support & Contact

Have questions or found an issue?
- 📧 Open a GitHub Issue with detailed description
- Include error messages and steps to reproduce
- Share your Python and library versions
- Attach relevant screenshots or logs

---

⭐ **If this project helped you, please consider giving it a star!**

Made with ❤️ by Naman Bhade
