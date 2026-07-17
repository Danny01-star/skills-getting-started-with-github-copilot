# Node.js Express Health Check Project

A simple Node.js Express server with a health check endpoint.

## Folder Structure

```
node-express-health-check/
├── src/
│   └── index.js          # Main application file
├── .env.example          # Environment variables template
├── .gitignore            # Git ignore file
├── package.json          # Project dependencies and scripts
└── README.md             # This file
```

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Danny01-star/skills-getting-started-with-github-copilot.git
cd skills-getting-started-with-github-copilot
```

2. Checkout the branch:
```bash
git checkout node-express-health-check
```

3. Install dependencies:
```bash
npm install
```

## Configuration

1. Create a `.env` file from the template:
```bash
cp .env.example .env
```

2. Edit `.env` if needed (default PORT is 3000)

## Running the Server

### Production mode:
```bash
npm start
```

### Development mode (with auto-reload):
```bash
npm run dev
```

The server will start on `http://localhost:3000`

## API Endpoints

### Health Check
- **URL:** `GET /health`
- **Response:**
```json
{
  "status": "ok",
  "timestamp": "2026-07-17T10:30:45.123Z",
  "uptime": 125.456
}
```

### Welcome
- **URL:** `GET /`
- **Response:**
```json
{
  "message": "Welcome to Node.js Express Server",
  "health_check": "Visit /health for status"
}
```

## Testing the Health Endpoint

Using curl:
```bash
curl http://localhost:3000/health
```

Using browser:
```
http://localhost:3000/health
```

Using Node.js fetch:
```javascript
fetch('http://localhost:3000/health')
  .then(res => res.json())
  .then(data => console.log(data));
```

## Dependencies

- **express:** ^4.18.2 - Web application framework
- **nodemon:** ^3.0.1 (dev) - Auto-restart server on file changes

## License

ISC
