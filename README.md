
<div align="center">

# PhantomPHP

**A Powerful PHP Development Server for Termux**

[![Version](https://img.shields.io/badge/version-1.0-blue?style=for-the-badge)](https://github.com/codetesla51/phantomphp/releases)
[![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)](LICENSE)
[![PHP Version](https://img.shields.io/badge/php-%3E%3D7.4-purple?style=for-the-badge)](https://php.net)

---

Run PHP & MySQL applications directly from your Android device

</div>

## Features

<table>
<tr>
<td width="50%">

**Development Tools**
- PHP server with live reload
- Direct file execution
- Custom port selection
- Automatic installation
</td>
<td width="50%">

**Database Integration**
- Built-in MySQL support
- phpMyAdmin interface
- Database management tools
- Secure connections
</td>
</tr>
</table>

## Prerequisites

**Required Software:**
- Termux ([F-Droid](https://f-droid.org) | [GitHub](https://github.com/termux/termux-app/releases))
- PHP 7.4 or higher
- Composer
- MariaDB
- phpMyAdmin

## Installation

1. **Install PhantomPHP:**
```bash
git clone https://github.com/codetesla51/phantomphp.git
cd phantomphp
chmod +x install
./install
```

2. **Verify Installation:**
```bash
phantom -v
```

## Usage Guide

### Start PHP Server
```bash
# Default port (8000)
phantom --serve

# Custom port
phantom --serve 8080
```

### Access Database
```bash
# Start phpMyAdmin
phantom --db 8080

# Access at: http://localhost:8080
# Username: root
# Password: root
```

### Run PHP Files
```bash
# Run a PHP file
phantom --run filename

# Example
phantom --run init
```

### Port Forwarding
```bash
# Start server with forwarding
phantom --serve 8080

# Press 'F' when prompted to enable forwarding
```

## Command Reference

<table>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
<tr>
<td><code>--serve [port]</code></td>
<td>Start PHP server (default: 8000)</td>
</tr>
<tr>
<td><code>--db [port]</code></td>
<td>Launch phpMyAdmin interface</td>
</tr>
<tr>
<td><code>--run [file]</code></td>
<td>Execute PHP file directly</td>
</tr>
<tr>
<td><code>-v</code></td>
<td>Display version information</td>
</tr>
<tr>
<td><code>--help</code></td>
<td>Show help menu</td>
</tr>
</table>

## Security Notes

- Always use strong passwords for database access
- Enable port forwarding only when necessary
- Keep Termux and all components updated
- Use HTTPS when possible

## Support

Need help? Contact us:
- Email: uoladele99@gmail.com
- GitHub Issues: [Open an issue](https://github.com/codetesla51/phantomphp/issues)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Submit a pull request

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

<div align="center">

---

**Found PhantomPHP helpful? Leave a star to show your support!**

[⭐ Star on GitHub](https://github.com/codetesla51/phantomphp)

</div>