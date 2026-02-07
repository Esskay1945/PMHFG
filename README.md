# 🌹 BloomInvite - Romantic Date Invitation Platform

> **A magical fusion of heartfelt invitations and procedural flower art**

## ✨ What is BloomInvite?

BloomInvite is a unique romantic web application that combines two powerful features:

1. **Ping My Heart** - Create personalized, heartwarming date invitations with custom messages and background music
2. **Petal Gift** - An interactive procedural flower animation engine that grows beautiful, physics-based flowers on canvas

When someone accepts your date invitation, they're rewarded with a stunning interactive flower garden where each tap grows unique, procedurally-generated flowers with realistic swaying animations and particle effects.

## 🎯 Live Demo

**🚀 The application is already live at:** [https://pmhfg.onrender.com/](https://pmhfg.onrender.com/)

Try it out and send someone special a magical invitation today!

## 🌟 Features

### Invitation System
- 📝 **Custom Messages** - Write personalized notes in a beautiful notebook-style interface
- 🎵 **Background Music** - Upload custom audio files for your invitation
- 🌸 **Flower Selection** - Choose from 12+ flower types (Rose, Sunflower, Lily, Tulip, Sakura, etc.)
- 🎨 **Color Customization** - Select rose colors (Red, Pink, White) for personalized gifts
- 📱 **Mobile Responsive** - Beautiful experience on all devices
- 🎁 **Gift Reveal** - Surprise transition from invitation to interactive flower garden

### Flower Engine
- 🌱 **Procedural Growth** - Watch flowers grow from stem to full bloom in real-time
- 🍃 **Organic Leaves** - Realistic leaf placement with petioles and veining
- 💨 **Physics-Based Sway** - Natural wind animations with time-based oscillations
- ✨ **Particle Effects** - Magical sparkles during flower growth
- 🎨 **Gradient Shading** - Realistic petal coloring with light-to-dark gradients
- 🖱️ **Interactive** - Tap/click anywhere to grow more flowers
- ⚡ **Performance Optimized** - Bloom caching and mobile-friendly frame rates

### Dashboard Features
- 👤 **User Authentication** - Secure login and registration system
- 📊 **Invite Management** - Track all your sent invitations and their status
- 🎉 **Real-time Updates** - Confetti celebration when invites are accepted
- 📋 **Status Tracking** - See pending, accepted, or rejected invitations
- 🔗 **Easy Sharing** - One-click copy shareable links

## 🛠️ Tech Stack

### Frontend
- **Vanilla JavaScript** - No framework dependencies
- **HTML5 Canvas** - For flower rendering engine
- **CSS3** - Glassmorphic design with animations
- **Canvas Confetti** - Celebration effects

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web server framework
- **Multer** - File upload handling
- **Helmet** - Security middleware
- **Express Rate Limit** - DDoS protection
- **XSS Clean** - Cross-site scripting prevention

### Storage
- **In-Memory Storage** - Fast, session-based data (Map structures)
- **File System** - Audio upload management

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/bloominvite.git

# Navigate to project directory
cd bloominvite

# Install dependencies
npm install

# Create .env file (optional)
echo "PORT=3000" > .env

# Start the server
npm start

# For development with auto-reload
npm run dev
```

## 🚀 Deployment

The application is deployed on **Render** and accessible at:
**https://pmhfg.onrender.com/**

To deploy your own instance:

1. Fork this repository
2. Create a new Web Service on [Render](https://render.com)
3. Connect your GitHub repository
4. Set the build command: `npm install`
5. Set the start command: `npm start`
6. Deploy!

## 📝 Usage

### Creating an Invitation

1. **Register/Login** - Create an account at `/login.html`
2. **Access Dashboard** - Navigate to your dashboard
3. **Customize Your Invite**:
   - Enter recipient's name
   - Write a personalized message
   - Upload background music (optional)
   - Choose a flower type
   - Select color (for roses)
   - Choose music for the flower view
4. **Generate Link** - Click "Generate Secret Link"
5. **Share** - Copy and send the link to your special someone

### Receiving an Invitation

1. **Open Link** - Click the shared invitation link
2. **Read Message** - Click the envelope to reveal the letter
3. **Respond** - Accept or decline the invitation
4. **Unlock Gift** - If accepted, click the gift box
5. **Grow Flowers** - Tap anywhere on screen to create beautiful flowers

## 🎨 Flower Types

- 🌹 **Rose** - Classic romantic flower with layered petals
- 🌻 **Sunflower** - Bright and cheerful yellow blooms
- 🪻 **Lily** - Elegant purple flowers
- 🌷 **Tulip** - Spring favorite with simple beauty
- 🌸 **Sakura** - Delicate cherry blossoms
- 🌿 **Lavender** - Multiple stems with calming vibes
- 🌼 **Daisy** - Pure white simplicity
- 🌺 **Hibiscus** - Tropical vibrant blooms
- 🪷 **Orchid** - Exotic and sophisticated
- 🌵 **Cactus** - Desert strength and resilience
- 🍁 **Maple** - Autumn warmth
- 🍀 **Clover** - Lucky charm symbolism

## 🔐 Security Features

- **Helmet.js** - Sets various HTTP headers for security
- **XSS Protection** - Sanitizes user inputs
- **Rate Limiting** - Prevents abuse and DDoS attacks
- **Input Validation** - Express-validator for all endpoints
- **File Type Checking** - Only audio files allowed for uploads
- **File Size Limits** - 10MB maximum upload size
- **Session Management** - Secure session handling with nanoid

## 📁 Project Structure

```
bloominvite/
├── public/
│   ├── dashboard.html      # Admin dashboard
│   ├── date.html           # Invitation view page
│   ├── login.html          # Login page
│   ├── register.html       # Registration page
│   ├── flower-engine.js    # Canvas flower animation engine
│   ├── style.css           # Global styles
│   └── uploads/            # User-uploaded audio files
├── server.js               # Express server & API
├── package.json            # Dependencies
├── .env                    # Environment variables
└── README.md              # This file
```

## 🎯 API Endpoints

### Authentication
- `POST /api/register` - Create new user account
- `POST /api/login` - Login and get session ID

### Invitations
- `POST /api/generate-link` - Create new invitation
- `GET /api/invites` - Get user's invitations (requires auth)
- `GET /api/get-link?id={linkId}` - Retrieve invitation details
- `POST /api/respond` - Accept/reject invitation

### File Upload
- `POST /api/upload-audio` - Upload background music (requires auth)

## 🌈 Flower Engine Architecture

The flower animation engine uses a class-based approach:

- **Flower Class** - Manages individual flower lifecycle
- **Particle Class** - Handles sparkle effects
- **Growth States** - stem → bud → bloom progression
- **Bloom Caching** - Renders complex petals to off-screen canvas for performance
- **Responsive Scaling** - Adjusts element sizes based on viewport width

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the ISC License.

## 💖 Acknowledgments

- Inspired by the beauty of nature and human connection
- Built with love for creating magical moments
- Thanks to the open-source community for amazing tools

## 🐛 Known Issues

- In-memory storage means data resets on server restart (consider implementing database for production)
- File uploads persist but aren't cleaned up automatically
- No email notifications for invitation responses (feature request)

## 🔮 Future Enhancements

- [ ] Database integration (MongoDB/PostgreSQL)
- [ ] Email notifications
- [ ] More flower types and animations
- [ ] Social sharing integrations
- [ ] Mobile app versions
- [ ] Scheduled invitations
- [ ] Custom themes and templates

---

Made with 💕 by [Your Name]

**Remember:** Every great love story starts with a simple invitation. Make yours magical! ✨
