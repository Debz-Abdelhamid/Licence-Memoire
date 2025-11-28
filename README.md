# 🩸 GoutteVie - Blood Donation Management System

[![PHP Version](https://img.shields.io/badge/PHP-8.2+-blue.svg)](https://php.net)
[![MySQL](https://img.shields.io/badge/MySQL-8.0+-orange.svg)](https://mysql.com)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.0+-purple.svg)](https://getbootstrap.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **"Unis pour la Vie : Ensemble pour le Don de Sang"** - United for Life: Together for Blood Donation

GoutteVie is a comprehensive web-based blood donation management system designed to connect donors, blood banks, and hospitals in Algeria. The platform simplifies the blood donation process by enabling donors to register, manage their accounts, and locate donation centers while facilitating coordination between blood banks and hospitals.

## 🌟 Features

### For Donors
- **User Registration & Authentication**: Secure signup with email verification
- **Profile Management**: Complete donor profile with blood type, medical history, and contact information
- **Donation Scheduling**: Book appointments at local blood banks or hospitals
- **Donation History**: Track all previous donations and eligibility status
- **Location Services**: Find nearby blood banks and donation centers using GPS
- **Blood Type Compatibility**: Automatic matching based on blood group requirements

### For Blood Banks & Hospitals
- **Inventory Management**: Real-time tracking of blood stock levels
- **Direct Requests**: Hospitals can request specific blood types directly from blood banks
- **Donor Coordination**: Manage donor appointments and blood collection
- **Quality Control**: Track blood processing and storage conditions
- **Reporting**: Generate reports on donation statistics and inventory levels

### System Features
- **Multi-language Support**: French interface optimized for Algerian users
- **Responsive Design**: Mobile-friendly interface using Bootstrap 5
- **Email Notifications**: Automated notifications for appointments and requests
- **Security**: Password hashing, session management, and input validation
- **Real-time Updates**: Live status updates for donations and requests

## 🛠️ Tech Stack

- **Backend**: PHP 8.2+
- **Database**: MySQL 8.0+
- **Frontend**: HTML5, CSS3, JavaScript
- **Framework**: Bootstrap 5.0+
- **Email**: PHPMailer
- **Maps**: Google Maps API integration
- **Security**: Password hashing with bcrypt

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **PHP 8.2 or higher**
- **MySQL 8.0 or higher**
- **Apache/Nginx web server**
- **Composer** (for dependency management)
- **Git**

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/goutte-vie.git
cd goutte-vie
```

### 2. Database Setup
```bash
# Create MySQL database
mysql -u root -p
CREATE DATABASE sang;
EXIT;

# Import database schema
mysql -u root -p sang < database/sang.sql
```

### 3. Configuration
Update the database configuration in `core/config.php`:
```php
define("HOST","localhost");
define("USER","your_db_user");
define("PASS","your_db_password");
define("DBNAME",'sang');
```

### 4. Web Server Configuration
- Place the project in your web server's root directory (e.g., `htdocs` for XAMPP)
- Ensure the `public/` directory is accessible via web browser
- Configure URL rewriting if using Apache with `.htaccess`

### 5. Email Configuration
Configure PHPMailer settings in `core/mailpass.php` for email notifications.

## 📖 Usage

### Accessing the Application
1. Open your web browser and navigate to `http://localhost/goutte-vie/public/`
2. Click "Inscrire" to register as a new donor
3. Or click "Connexion" to login with existing credentials

### User Roles
- **Donor**: Register, schedule donations, view history
- **Blood Bank**: Manage inventory, process requests
- **Hospital**: Request blood, manage patient needs

### Key Workflows
1. **Donor Registration**: Complete profile with personal and medical information
2. **Appointment Booking**: Select location and preferred date/time
3. **Blood Requests**: Hospitals submit requests to blood banks
4. **Inventory Updates**: Real-time stock level monitoring

## 📁 Project Structure

```
goutte-vie/
├── core/                    # Core PHP files
│   ├── autoloading.php     # Class autoloader
│   ├── config.php          # Database configuration
│   ├── connexion.php       # Database connection
│   ├── filltring.php       # Input filtering
│   ├── mailsend.php        # Email sending functions
│   ├── mailpass.php        # Email configuration
│   └── sessionprotection.php # Session security
├── database/               # Database files
│   └── sang.sql           # Database schema and sample data
├── public/                 # Public web files
│   ├── index.php          # Homepage
│   ├── login.php          # Login page
│   ├── inscription.php    # Registration page
│   ├── css/               # Stylesheets
│   ├── js/                # JavaScript files
│   ├── images/            # Image assets
│   └── fonts/             # Custom fonts
└── README.md              # Project documentation
```

## 🔧 API Endpoints

The application includes several AJAX endpoints for dynamic content:

- `get_don_disponible.php` - Get available donations
- `get_notification.php` - User notifications
- `valide_demmande.php` - Validate donation requests
- `chercher_donneur.php` - Search donors

## 🤝 Contributing

We welcome contributions to GoutteVie! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Follow PSR-12 coding standards
- Write descriptive commit messages
- Test thoroughly before submitting PRs
- Update documentation for new features

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

**GoutteVie Team**
- **Email**: goutteviedz@gmail.com
- **Phone**: +213 7 95 33 75 74
- **Location**: Annaba, Algeria

**Project Links**
- **Website**: [goutte-vie.com](https://goutte-vie.com)
- **Facebook**: [GoutteVie Official](https://facebook.com/gouttevie)
- **Instagram**: [GoutteVie Official](https://instagram.com/gouttevie)

## 🙏 Acknowledgments

- **Algerian Ministry of Health** for supporting blood donation initiatives
- **Local Blood Banks** for their collaboration
- **Open Source Community** for the tools and libraries used

## 📊 Statistics

- **Target**: 10,000 blood donations per day in Algeria
- **Current Coverage**: Supporting hospitals across Annaba and surrounding regions
- **Impact**: Helping save lives through efficient blood management

---

**Made with ❤️ in Annaba, Algeria** 🇩🇿

*"Chaque goutte compte, chaque vie importe"* - Every drop counts, every life matters
