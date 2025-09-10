# Linky 🔗

A simple and efficient link management application designed for easy deployment across multiple platforms.

## Features

- Simple web interface
- RESTful API endpoints
- Health monitoring
- Docker support
- Multiple deployment options

## Quick Start

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/mymy3399/Linky.git
   cd Linky
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the application**
   ```bash
   npm start
   ```

The application will be available at `http://localhost:3000`

### API Endpoints

- `GET /` - Main application interface
- `GET /health` - Health check endpoint
- `GET /api/status` - Service status information

## Deployment Options

### 1. Docker Deployment

**Build and run with Docker:**
```bash
docker build -t linky .
docker run -p 3000:3000 linky
```

**Or use Docker Compose:**
```bash
docker-compose up -d
```

### 2. Vercel Deployment

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/mymy3399/Linky)

Or manually:
```bash
npm install -g vercel
vercel
```

### 3. Manual Deployment

1. **Prepare the server:**
   ```bash
   npm ci --production
   ```

2. **Set environment variables:**
   ```bash
   export NODE_ENV=production
   export PORT=3000
   ```

3. **Start the application:**
   ```bash
   npm start
   ```

### 4. Cloud Platform Deployment

The application is ready to deploy on:

- **Heroku**: Use the included `package.json` with start script
- **AWS ECS/Fargate**: Use the Docker configuration
- **Google Cloud Run**: Use the Docker configuration
- **Azure Container Instances**: Use the Docker configuration
- **DigitalOcean App Platform**: Use the Docker configuration

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `PORT` | Server port | `3000` |
| `NODE_ENV` | Environment mode | `development` |

## Health Monitoring

The application includes built-in health monitoring:

- **Health Check**: `GET /health`
- **Status API**: `GET /api/status`
- **Docker Health Check**: Configured in Dockerfile

## CI/CD

The repository includes GitHub Actions workflow for:

- Automated testing
- Docker image building
- Deployment pipeline

## Development

**Scripts available:**
- `npm start` - Start the application
- `npm run dev` - Start in development mode
- `npm run build` - Build the application
- `npm test` - Run tests
- `npm run lint` - Run linting

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and linting
5. Submit a pull request

## License

MIT License - see LICENSE file for details