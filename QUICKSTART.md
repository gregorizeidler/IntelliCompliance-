# 🚀 IntelliCompliance - Quick Start Guide

Get IntelliCompliance up and running in under 5 minutes!

## ⚡ Instant Setup

### 1. Clone & Install
```bash
git clone https://github.com/yourusername/IntelliCompliance.git
cd IntelliCompliance
npm install
```

### 2. Start the Server
```bash
npm start
```

### 3. Open in Browser
```
http://localhost:3000
```

That's it! 🎉

## 🔍 What You Get

- **17,000+ Real OFAC Sanctions Data** - Automatically collected
- **AI-Powered Risk Analysis** - Instant risk scoring
- **Professional Web Interface** - Modern, responsive design
- **Advanced Search** - Multi-criteria filtering
- **Real-time Statistics** - Live dashboard
- **RESTful API** - Complete API endpoints

## 🎯 Key Features Demo

### Search Sanctions
```bash
# Search for entities
curl "http://localhost:3000/api/search?q=terrorism"

# Filter by jurisdiction
curl "http://localhost:3000/api/search?jurisdiction=OFAC"

# Filter by risk level
curl "http://localhost:3000/api/search?risk=High"
```

### Check System Health
```bash
curl http://localhost:3000/api/health
```

### Get Statistics
```bash
curl http://localhost:3000/api/statistics
```

### Export Data
```bash
curl http://localhost:3000/api/export > sanctions_data.json
```

## 📊 Web Interface

Navigate to `http://localhost:3000` to access:

- **🏠 Dashboard**: Real-time statistics and KPIs
- **🔍 Search**: Advanced multi-criteria search
- **📈 Analytics**: Risk analysis and patterns
- **⚙️ Settings**: Configuration options

## 🐳 Docker Quick Start

### Option 1: Simple Docker
```bash
docker build -t intellicompliance .
docker run -p 3000:3000 intellicompliance
```

### Option 2: Docker Compose (Full Stack)
```bash
docker-compose up --build
```

## 🔧 Configuration

### Environment Variables
Copy `env.example` to `.env` and customize:
```bash
cp env.example .env
```

### Key Settings
- `PORT=3000` - Server port
- `AUTO_UPDATE_ENABLED=true` - Auto data updates
- `MAX_ENTITIES_LIMIT=0` - Entity limit (0 = no limit)

## 📱 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/health` | GET | System health check |
| `/api/search` | GET | Search sanctions data |
| `/api/statistics` | GET | Get system statistics |
| `/api/refresh` | POST | Refresh data manually |
| `/api/export` | GET | Export data |

## 🔍 Search Parameters

| Parameter | Type | Description | Example |
|-----------|------|-------------|---------|
| `q` | string | Search query | `?q=terrorism` |
| `jurisdiction` | string | Filter by jurisdiction | `?jurisdiction=OFAC` |
| `type` | string | Entity type | `?type=Individual` |
| `risk` | string | Risk level | `?risk=High` |
| `limit` | number | Results limit | `?limit=100` |
| `offset` | number | Results offset | `?offset=50` |

## 📈 Sample Queries

### Find High-Risk Entities
```bash
curl "http://localhost:3000/api/search?risk=Critical&limit=10"
```

### Search Specific Programs
```bash
curl "http://localhost:3000/api/search?q=terrorism&jurisdiction=OFAC"
```

### Get Recent Additions
```bash
curl "http://localhost:3000/api/search?sort=date&order=desc&limit=20"
```

## 🎨 UI Features

### Dashboard Cards
- **Total Entities**: Live count of all sanctions
- **Jurisdictions**: Number of active jurisdictions
- **Risk Distribution**: High/Medium/Low risk breakdown
- **Last Update**: Data freshness indicator

### Search Interface
- **Smart Search**: Intelligent query processing
- **Real-time Results**: Instant search as you type
- **Advanced Filters**: Multiple criteria selection
- **Export Options**: Download results in JSON

### Analytics
- **Risk Analysis**: AI-powered risk scoring
- **Pattern Detection**: Suspicious activity identification
- **Trend Analysis**: Historical data patterns
- **Geographic Distribution**: Location-based insights

## 🛠️ Development

### Start Development Server
```bash
npm run dev
```

### Run Tests
```bash
npm test
```

### Check Security
```bash
npm run security
```

### Monitor Performance
```bash
npm run monitor
```

## 🔄 Data Updates

### Automatic Updates
- Updates every hour by default
- Configurable interval via `DATA_UPDATE_INTERVAL`
- Real-time status in dashboard

### Manual Updates
```bash
# Via API
curl -X POST http://localhost:3000/api/refresh

# Via npm script
npm run data:refresh
```

## 🚨 Troubleshooting

### Port Already in Use
```bash
# Kill existing processes
lsof -ti:3000 | xargs kill -9

# Or use different port
PORT=3001 npm start
```

### Memory Issues
```bash
# Increase Node.js memory limit
node --max-old-space-size=4096 server.js
```

### Data Loading Slow
- Check internet connection
- Verify OFAC API availability
- Consider reducing `MAX_ENTITIES_LIMIT`

## 📚 Next Steps

1. **Read the [README.md](README.md)** for detailed documentation
2. **Check [CONTRIBUTING.md](CONTRIBUTING.md)** to contribute
3. **Review [API Documentation](README.md#api-documentation)** for integration
4. **Explore [Configuration Options](README.md#configuration)** for customization

## 🆘 Need Help?

- **Documentation**: Check README.md for detailed info
- **Issues**: Create GitHub issue for bugs
- **Features**: Request new features via GitHub
- **API**: Use `/api/health` to verify system status

## 🎯 Production Deployment

### Environment Setup
```bash
# Set production environment
export NODE_ENV=production
export PORT=80

# Start with PM2 (recommended)
npm install -g pm2
pm2 start server.js --name intellicompliance
```

### Security Checklist
- [ ] Set strong `SESSION_SECRET`
- [ ] Configure proper `CORS_ORIGIN`
- [ ] Enable HTTPS in production
- [ ] Set up firewall rules
- [ ] Configure monitoring

---

## 🎉 You're Ready!

IntelliCompliance is now running with:
- ✅ Real sanctions data
- ✅ AI risk analysis
- ✅ Professional interface
- ✅ Complete API
- ✅ Multi-jurisdiction support

**Happy compliance monitoring!** 🛡️ 