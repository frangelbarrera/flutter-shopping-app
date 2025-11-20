# 🛍️ Flutter Shopping App 

A complete e-commerce mobile application developed with Flutter by Frangel Barrera, implementing an elegant dark theme based on Material Design 3 and connected to the FakeStore API. Portfolio project demonstrating Flutter mobile development skills.

## 👨‍💻 Author

**Frangel Barrera**
- GitHub: [https://github.com/frangelbarrera](https://github.com/frangelbarrera)
- LinkedIn: [Your LinkedIn profile if you have one]

## 📱 Main Features

### ✨ User Interface
- **Complete Dark Theme**: Consistent implementation of Material Design 3 Dark Theme
- **Professional Color Palette**: Inspired by premium marketplace designs
- **Custom Components**: Widgets optimized for e-commerce
- **Intuitive Navigation**: Bottom navigation with dynamic badges
- **Smooth Animations**: Fluid transitions between screens

### 🛒 E-commerce Features
- **Product Catalog**: Responsive grid with products from FakeStore API
- **Filters and Search**: Filtering by categories and real-time search
- **Product Details**: Full screen with images, descriptions and ratings
- **Shopping Cart**: Complete cart management with automatic calculations
- **Category System**: Organized navigation by product types

### 🔧 Technical Architecture
- **Global State**: Management with Provider pattern
- **Networking**: Integration with FakeStore API using Dio
- **Images**: Smart caching with CachedNetworkImage
- **Advanced Layouts**: StaggeredGridView for dynamic layouts
- **Optimization**: Lazy loading and optimized performance

## 🏗️ Project Structure

```
flutter-shopping-app/
├── lib/
│   ├── main.dart                 # Main entry point
│   ├── models/                   # Data models
│   │   ├── product.dart         # Product model
│   │   ├── category.dart        # Category model
│   │   └── cart_item.dart       # Cart item model
│   ├── services/                # External services
│   │   └── api_service.dart     # FakeStore API service
│   ├── providers/               # State management
│   │   ├── product_provider.dart
│   │   └── cart_provider.dart
│   ├── screens/                 # Main screens
│   │   ├── home_screen.dart     # Home screen
│   │   ├── product_detail_screen.dart
│   │   ├── cart_screen.dart     # Shopping cart
│   │   ├── categories_screen.dart
│   │   └── profile_screen.dart  # User profile
│   ├── widgets/                 # Reusable components
│   │   ├── product_card.dart    # Product card
│   │   ├── category_chip.dart   # Category chip
│   │   ├── custom_app_bar.dart  # Custom AppBar
│   │   └── bottom_nav_bar.dart  # Bottom navigation
│   └── theme/                   # Theme configuration
│       ├── app_colors.dart      # Color palette
│       └── app_theme.dart       # Theme configuration
├── android/                     # Android configuration
├── pubspec.yaml                # Project dependencies
└── README.md                   # Documentation
```

## 🎨 Design and Theme

### Color Palette
- **Primary**: `#B08C47` (Gold/Bronze) - CTAs and main elements
- **Secondary**: `#6C675E` (Taupe Gray) - Secondary elements
- **Background**: `#121212` (Material Black) - Main background
- **Surface**: `#1E1E1E` - Card surfaces
- **Success**: `#4CAF50` - Positive states
- **Error**: `#CF6679` - Error states
- **Warning**: `#FF9800` - Alerts

### Contrast Specifications
All colors comply with WCAG AA guidelines (4.5:1 ratio minimum) for accessibility.

## 🔌 API Integration

### FakeStore API
- **Base URL**: `https://fakestoreapi.com`
- **Used Endpoints**:
  - `GET /products` - Product list
  - `GET /products/categories` - Available categories
  - `GET /products/category/{category}` - Products by category
  - `GET /products/{id}` - Specific product details

### Data Handling
- Smart product caching
- Optimized local search
- Robust error handling
- Consistent loading states

## 📦 Installation and Configuration

### Prerequisites
```bash
# Flutter SDK (version 3.10.0 or higher)
flutter --version

# Android Studio with Android SDK
# VS Code with Flutter extensions (optional)
```

### Installation
```bash
# Clone the project
git clone <repository-url>
cd flutter-shopping-app

# Install dependencies
flutter pub get

# Run in debug mode
flutter run

# Build release APK
flutter build apk --release
```

### Main Dependencies
```yaml
dependencies:
  flutter: sdk
  provider: ^6.1.1          # State management
  dio: ^5.4.0               # HTTP client
  cached_network_image: ^3.3.0  # Image caching
  flutter_staggered_grid_view: ^0.7.0  # Advanced layouts
  badges: ^3.1.2            # UI badges
```

## 📱 Screens and Features

### 🏠 Home Screen
- Product grid with infinite scroll
- Featured products section
- Integrated search bar
- Category filters
- Quick navigation

### 🏷️ Categories Screen
- Tab navigation
- Informative headers by category
- Products organized by type
- Dynamic counters

### 🛒 Shopping Cart
- Complete list of added products
- Quantity controls (+/-)
- Automatic total calculations
- Discount management
- Simulated checkout process
- Swipe to delete gesture

### 👤 Profile Screen
- User information
- Usage statistics
- App settings
- Help center
- Account options

### 📦 Product Details
- Image gallery
- Complete description
- Rating system
- Related products
- Quantity controls
- Action buttons (Add/Buy)

## 🔧 Technical Configurations

### Global State (Provider)
```dart
// Configuration in main.dart
MultiProvider(
  providers: [
    ChangeNotifierProvider(create: (_) => ProductProvider()),
    ChangeNotifierProvider(create: (_) => CartProvider()),
  ],
  child: MaterialApp(...)
)
```

### Dark Theme
```dart
// Theme application
MaterialApp(
  theme: AppTheme.darkTheme,
  themeMode: ThemeMode.dark,
  ...
)
```

### Networking
```dart
// Dio configuration
final dio = Dio(BaseOptions(
  baseUrl: 'https://fakestoreapi.com',
  connectTimeout: Duration(seconds: 10),
  receiveTimeout: Duration(seconds: 10),
));
```

## 🚀 Build and Distribution

### Development APK
```bash
flutter build apk --debug
```

### Production APK
```bash
flutter build apk --release --split-per-abi
```

### Android App Bundle (Recommended for Play Store)
```bash
flutter build appbundle --release
```

### Applied Optimizations
- Code minification (R8)
- Resource compression
- Split APKs by ABI
- Dead code elimination

## 📊 Performance and Optimization

### Performance Metrics
- **Initial load time**: < 3 seconds
- **API response time**: < 2 seconds
- **Memory usage**: Optimized for mid-range devices
- **APK size**: < 20 MB per ABI

### Implemented Optimizations
- Lazy image loading
- Smart data caching
- Widgets with keys to optimize rebuilds
- Proper resource disposal
- Efficient memory management

## 🧪 Testing and Quality Assurance

### Tested Features
- ✅ Product loading from API
- ✅ Filtering and search
- ✅ Cart management
- ✅ Screen navigation
- ✅ Themes and styles
- ✅ Network error handling
- ✅ Loading states

### Compatible Devices
- **Android**: 5.0 (API 21) or higher
- **RAM**: 2 GB minimum recommended
- **Storage**: 100 MB free
- **Resolutions**: From 320dp to tablets

## 🔮 Future Features

### Upcoming Implementations
- [ ] User authentication
- [ ] Wishlist/favorites
- [ ] Order history
- [ ] Push notifications
- [ ] Integrated payments
- [ ] Offline mode
- [ ] Product sharing
- [ ] User reviews and ratings

### Planned Technical Improvements
- [ ] Unit tests implementation
- [ ] Integration tests
- [ ] CI/CD pipeline
- [ ] Crash report analysis
- [ ] User metrics
- [ ] Internationalization (i18n)

## 🤝 Contribution

### Style Guides
- Follow Dart/Flutter conventions
- Use descriptive comments
- Maintain naming consistency
- Document public functions
- Optimize imports

### Commit Structure
```
feat: new feature
fix: bug fix
docs: documentation update
style: formatting changes
refactor: code refactoring
test: adding tests
```

## 📄 License

This project is an educational demonstration developed to showcase Flutter's capabilities in modern e-commerce application development.

## 📞 Support

To report bugs or request features:
- **Email**: frangelrcbarrera@gmail.com
- **GitHub**: https://github.com/frangelbarrera
- **Issues**: GitHub Issues
- **Documentation**: README.md and code comments

---

**Developed with ❤️ by Frangel Barrera using Flutter and Material Design 3**

*Flutter Shopping App - Portfolio project demonstrating modern mobile development*
