# 🔮 Crystal Ball Age Predictor

A mystical web application that predicts your age based on your name using the power of data science and a touch of magic! ✨

![Crystal Ball Demo](https://github.com/NurG001/CrystalBall.github.io/blob/main/assets/Icon.png)

## 🌟 Features

- **🔮 Magical Interface**: Beautiful glassmorphism design with animated crystal ball
- **📊 Age Prediction**: Uses the Agify API to predict age based on name frequency data
- **🎯 Age Categories**: Categorizes predictions into fun age groups
- **📝 Prediction History**: Tracks your last 5 predictions with timestamps
- **🔄 Dynamic Placeholders**: Cycling name suggestions to inspire your next prediction
- **⚡ Real-time Validation**: Input validation with helpful error messages
- **📱 Responsive Design**: Works seamlessly on desktop and mobile devices

## 🎨 Design Highlights

- **Glassmorphism Effects**: Modern blur and transparency effects
- **Gradient Backgrounds**: Eye-catching color gradients
- **Smooth Animations**: Floating crystal ball and loading spinners
- **Interactive Elements**: Hover effects and responsive buttons

## 🔧 How It Works

### 1. Structure (HTML)
The app consists of:
- A decorative animated crystal ball (🔮)
- Title and subtitle sections
- Name input field with validation
- Prediction trigger button
- Loading spinner for API calls
- Results container with age and confidence display
- History section showing last 5 predictions
- Footer with credits

### 2. Styling (CSS)
Modern UI techniques include:
- **Glassmorphism**: `backdrop-filter: blur()` for container styling
- **Gradient backgrounds** for buttons and body
- **Animations**: Floating crystal ball, spinning loader
- **Responsive layout**: Flexbox centering and mobile-friendly design

### 3. Functionality (JavaScript)

#### 🔍 Name Input & Validation
```javascript
if (!/^[a-zA-Z\s-']+$/.test(name)) {
    showError('Please enter a valid name (letters only)!');
}
```
- Only allows alphabetic names (plus hyphen, space, apostrophe)
- Enter key triggers prediction

#### 🔮 Age Prediction Logic
```javascript
const response = await fetch(`https://api.agify.io?name=${encodeURIComponent(name)}`);
```
- Sends request to Agify API
- Receives JSON response with age prediction and confidence data

#### 📊 Age Categories
- 👶 **Young Spirit** (≤ 12)
- 🌟 **Teenage Energy** (13–19)
- 💪 **Young Adult** (20–35)
- 🎯 **Prime Years** (36–55)
- 🧙♂️ **Wise Soul** (56+)

#### 🕰️ History Tracking
```javascript
predictionHistory.unshift({ name, age, count, timestamp });
```
- Stores last 5 predictions in memory
- Displays with timestamps in history section

#### 🔁 Dynamic Placeholders
- Cycles through sample names every 3 seconds
- Only when input field is empty
- Suggests interesting names to try

## 🚀 How to Run

### Option 1: Direct File Opening
1. **Download the files**:
   ```bash
   git clone https://github.com/yourusername/crystal-ball-age-predictor.git
   cd crystal-ball-age-predictor
   ```

2. **Open in browser**:
   - Simply double-click the `index.html` file
   - Or right-click → "Open with" → Your preferred browser

### Option 2: Local Server (Recommended)
For the best experience, run a local server:

#### Using Python:
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

#### Using Node.js:
```bash
# Install a simple server globally
npm install -g http-server

# Run the server
http-server
```

#### Using Live Server (VS Code Extension):
1. Install the "Live Server" extension in VS Code
2. Right-click on `index.html`
3. Select "Open with Live Server"

### Option 3: Online Hosting
Deploy to any static hosting service:
- **GitHub Pages**: Push to GitHub and enable Pages
- **Netlify**: Drag and drop your files
- **Vercel**: Connect your GitHub repository
- **Surge.sh**: Simple command-line deployment

## 🎮 Usage Example

1. **Enter a name**: Type "Sofia" in the input field
2. **Click "Reveal the Age"**: The crystal ball begins its magic
3. **View results**: 
   - Age: 23
   - Confidence: 1,323 oracle consultations
   - Category: 💪 Young Adult
4. **Check history**: Your prediction appears in the history section

## 🛠️ Technical Details

- **Frontend**: Pure HTML, CSS, and JavaScript (no frameworks)
- **API**: [Agify.io](https://agify.io/) for age predictions
- **Styling**: Modern CSS with glassmorphism and gradients
- **Animations**: CSS keyframes and transitions
- **Responsive**: Mobile-first design approach

## 📁 File Structure

```
crystal-ball-age-predictor/
├── index.html          # Main HTML file with embedded JavaScript
├── style.css           # CSS
└── README.md           # This file
```

## 🔮 API Information

This app uses the [Agify.io API](https://agify.io/):
- **Endpoint**: `https://api.agify.io?name={name}`
- **Rate limit**: 1000 requests per day (free tier)
- **Response format**: `{"name": "john", "age": 57, "count": 12345}`

## 🎯 Browser Compatibility

- ✅ Chrome (80+)
- ✅ Firefox (75+)
- ✅ Safari (13+)
- ✅ Edge (80+)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Credits

- **Agify API** for providing age prediction data
- **Design inspiration** from modern glassmorphism trends
- **Icons** from Unicode emoji set

## 🔗 Links

- [Live Demo](https://nurg001.github.io/CrystalBall.github.io/)
- [Agify.io API Documentation](https://agify.io/)

---

**✨ May the crystal ball reveal your digital age with mystical accuracy! ✨**
