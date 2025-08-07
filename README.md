# Smart IP AutoFill Chrome Extension

A powerful and secure Chrome extension that intelligently captures and autofills form data across websites. Save time with reusable profiles stored securely in your browser with Google authentication.

## ✨ Features

### 🔐 **Secure & Private**
- **Local Storage Only**: All data stays on your device - never sent to external servers
- **Google OAuth Authentication**: Secure login with your Google account
- **Encrypted Storage**: Your form data is encrypted and protected
- **Privacy-First**: No tracking, no data collection, no external transmission

### 🎯 **Smart Form Detection**
- **Intelligent Field Recognition**: Automatically detects form fields using multiple strategies
- **Cross-Platform Support**: Works on any website with forms
- **Smart Click Simulation**: Properly handles radio buttons and checkboxes to trigger JavaScript events
- **Enhanced Dropdown Support**: Handles single-select and multi-select dropdowns with smart matching

### 🔄 **Adaptive URL Filling**
- **Facebook/Instagram Mode**: Optimized for social media platforms with one URL per field (30 URL limit)
- **General Mode**: Flexible URL filling for all other websites with no artificial limits
- **Smart URL Detection**: Automatically finds URL-related fields on any website

### 📱 **Modern User Interface**
- **Clean Design**: Intuitive, responsive interface with smooth animations
- **Real-time Feedback**: Instant visual feedback for all actions
- **Error Handling**: Comprehensive error messages and recovery options
- **Accessibility**: Keyboard navigation and screen reader support

## 🚀 Quick Start

### Installation

1. **Download** the extension files to your computer
2. **Open Chrome** and navigate to `chrome://extensions/`
3. **Enable Developer Mode** (toggle in top-right corner)
4. **Click "Load unpacked"** and select the extension folder
5. **Sign in** with your Google account to get started

### First Use

1. **Navigate** to any website with forms
2. **Fill out** the forms with your information
3. **Click** the Smart IP AutoFill icon in your toolbar
4. **Click "Create New AutoFill"** to save your data
5. **Enter a profile name** and capture your form data
6. **Review and save** your profile for future use

## 📖 Detailed Usage Guide

### Creating AutoFill Profiles

1. **Prepare Your Data**: Fill out forms on any website with the information you want to save
2. **Open Extension**: Click the Smart IP AutoFill icon in your Chrome toolbar
3. **Create Profile**: Click "Create New AutoFill" and enter a descriptive name
4. **Capture Data**: Click "Capture AutoFill Data" to collect form information
5. **Review & Edit**: Review the captured data and edit if needed
6. **Save Profile**: Click "Save Profile" to store your data securely

### Using AutoFill

1. **Navigate to Target Site**: Go to any website where you want to fill forms
2. **Open Extension**: Click the Smart IP AutoFill icon
3. **Select Profile**: Click "AutoFill Now" and choose a saved profile
4. **Add URLs** (if needed): Enter URLs you want to fill in the form
5. **Apply Profile**: Click "Fill Out Now" to automatically populate the form

### URL Filling Modes

#### Facebook/Instagram Mode
- **Automatic Detection**: Extension detects Facebook/Instagram sites automatically
- **URL Counter**: Shows "X/30 URLs" with 30 URL limit
- **One URL Per Field**: Each textarea receives one URL
- **Optimized Strategy**: Designed for social media platform requirements

#### General Mode
- **All Other Sites**: Works on any website not detected as social media
- **URL Counter**: Shows "X URLs" with no artificial limit
- **Smart Distribution**: All URLs filled together in URL-related fields
- **Flexible Strategy**: Adapts to different website structures

## 🔧 Technical Details

### Architecture

```
Smart IP AutoFill/
├── manifest.json          # Extension configuration
├── popup.html            # Main user interface
├── popup.css             # Styling and animations
├── popup.js              # Core functionality
├── content.js            # Web page interaction
├── background.js         # Background service worker
├── auth-handler.js       # Google OAuth authentication
├── icons/                # Extension icons
│   ├── icon-16.png
│   ├── icon-48.png
│   └── icon-128.png
├── utils/                # Utility modules
│   ├── security.js       # Security utilities
│   ├── logger.js         # Logging system
│   ├── init.js           # Initialization
│   └── ...               # Additional utilities
└── README.md            # This documentation
```

### Permissions Explained

| Permission | Purpose | Usage |
|------------|---------|-------|
| `activeTab` | Access current tab | Capture and fill form data on active webpage |
| `storage` | Save user data | Store autofill profiles locally on device |
| `scripting` | Execute scripts | Inject content scripts for form interaction |
| `identity` | Google OAuth | Secure user authentication and data isolation |

### Security Features

- **Local Storage**: All data stored locally using Chrome's encrypted storage
- **Google OAuth**: Secure authentication with industry-standard protocols
- **No External Calls**: Zero data transmission to external servers
- **Input Validation**: Comprehensive validation for all user inputs
- **XSS Protection**: Sanitization of all form data
- **CSRF Protection**: Built-in cross-site request forgery protection

## 🛡️ Privacy & Security

### Data Handling
- **Local Storage Only**: All form data remains on your device
- **Encrypted Storage**: Data is encrypted using Chrome's secure APIs
- **User Control**: Complete control over your data - view, edit, delete anytime
- **No Tracking**: Zero analytics, tracking, or data collection
- **Account Isolation**: Data is isolated per Google account

### Privacy Compliance
- **GDPR Compliant**: Follows European data protection regulations
- **CCPA Compliant**: Meets California consumer privacy requirements
- **Chrome Web Store Compliant**: Adheres to all store policies
- **Transparent Permissions**: Clear explanation of all permission usage

## 🔍 Troubleshooting

### Common Issues

**Extension Not Loading**
- Ensure Developer Mode is enabled in Chrome
- Check that all files are present in the directory
- Verify manifest.json syntax is correct

**Form Data Not Captured**
- Make sure the webpage has actual form elements
- Check that fields have names, IDs, or labels
- Try refreshing the page and filling forms again
- Ensure you're on a page with input fields

**Authentication Issues**
- Clear browser cache and cookies
- Sign out and sign back in with Google
- Check your internet connection
- Verify Google account permissions

**Storage Problems**
- Check Chrome's storage quota in chrome://settings/content
- Clear extension data if needed
- Verify storage permissions are granted

### Performance Tips

- **Regular Cleanup**: Delete unused profiles to free storage space
- **Profile Organization**: Use descriptive names for easy identification
- **URL Management**: Keep URL lists manageable for better performance
- **Browser Updates**: Keep Chrome updated for best compatibility

## 📋 System Requirements

- **Chrome Browser**: Version 88 or higher
- **Operating System**: Windows, macOS, or Linux
- **Internet Connection**: Required for Google OAuth authentication
- **Storage**: Minimum 10MB available space
- **Permissions**: Active tab and storage access

## 🔄 Version History

### v1.0.1 (Current)
- Enhanced security and privacy features
- Improved form detection algorithms
- Better error handling and recovery
- Performance optimizations
- Comprehensive logging system

### v1.0.0
- Initial release with core functionality
- Google OAuth authentication
- Basic form capture and autofill
- Facebook/Instagram URL handling

## 🤝 Support & Feedback

### Getting Help
- **Documentation**: Check this README for detailed instructions
- **Privacy Policy**: See `PRIVACY_POLICY.md` for data handling details
- **Permissions**: Review `PERMISSIONS_JUSTIFICATION.md` for permission explanations

### Reporting Issues
- **Bug Reports**: Document the issue with steps to reproduce
- **Feature Requests**: Describe the desired functionality
- **Security Concerns**: Report any security-related issues immediately

### Contributing
- **Code Quality**: Follow existing code style and patterns
- **Testing**: Test thoroughly before submitting changes
- **Documentation**: Update documentation for any new features

## 📄 Legal Information

### License
This project is open source and available under the MIT License.

### Terms of Service
- Use at your own risk
- No warranty provided
- Extension may be updated without notice
- Users are responsible for their data

### Privacy Policy
See `PRIVACY_POLICY.md` for complete privacy information.

---

**Smart IP AutoFill** - Secure, Private, and Intelligent Form Management

*Built with ❤️ for productivity and privacy* 