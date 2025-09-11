# Design Tokens Usage Tracker

A comprehensive dashboard for tracking design tokens usage across teams and digital channels. Built for Canon Design System teams to monitor adoption, manage changes, and ensure consistency across all digital properties.

## 🎯 Features

### MVP Features (Implemented)
- ✅ **Basic Token Usage Scanner** - Automated scanning of repositories for token usage
- ✅ **Simple Dashboard** - Overview of top used tokens and system metrics
- ✅ **Email Notifications** - Alerts for major token changes
- ✅ **Manual Approval Workflow** - Review and approve token changes

### Core Capabilities
- 📊 **Track Team Usage** - Monitor which teams and digital channels use design tokens
- 🔍 **Channel Monitoring** - Track design token usage across websites and apps
- 📈 **Pattern Analytics** - Monitor patterns and their token dependencies
- 👥 **Contributor Management** - Track design system contributors and their changes
- 🔔 **Smart Notifications** - Email and dashboard notifications for token updates
- ✅ **Approval System** - Review and approval workflow for incoming changes
- 🧪 **Test Deployment** - Deploy changes to test environments before production

## 🏗️ Architecture

```
├── frontend/          # React TypeScript dashboard
├── backend/           # Node.js API server
├── shared/            # Shared types and utilities
├── database/          # Prisma schema and migrations
└── docs/              # Documentation
```

### Tech Stack
- **Frontend**: React 18 + TypeScript + Tailwind CSS
- **Backend**: Node.js + Express + TypeScript
- **Database**: PostgreSQL + Prisma ORM
- **Cache**: Redis (optional)
- **Real-time**: WebSocket (Socket.io)
- **Charts**: Chart.js + D3.js

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- PostgreSQL 14+
- Redis (optional, for caching)

### Installation

1. **Clone and install dependencies**
   ```bash
   git clone <repository-url>
   cd ds-usage-tracker
   npm run install:all
   ```

2. **Setup environment files**
   ```bash
   # Backend
   cd backend
   cp .env.example .env
   # Edit .env with your database and service credentials
   
   # Frontend  
   cd ../frontend
   cp .env.example .env
   ```

3. **Setup database**
   ```bash
   cd ../backend
   npx prisma migrate dev
   npx prisma db seed
   ```

4. **Start development servers**
   ```bash
   cd ..
   npm run dev
   ```

The dashboard will be available at `http://localhost:3000` and the API at `http://localhost:5000`.

## 📖 Usage

### Dashboard Overview
- View system-wide token usage metrics
- Monitor team adoption scores
- Track recent activity and changes
- Identify deprecated tokens requiring attention

### Token Management
- Scan repositories for token usage
- View detailed token dependency graphs
- Track usage trends over time
- Manage token lifecycles

### Team Collaboration
- Review and approve token changes
- Test changes in staging environments
- Receive notifications for relevant updates
- Track team-specific adoption metrics

## 🔧 Configuration

### Scanning Configuration
Configure which repositories and file types to scan:

```javascript
// backend/src/config/scanner.js
module.exports = {
  repositories: [
    'https://github.com/canon/marketing-web',
    'https://github.com/canon/e-commerce-app'
  ],
  fileTypes: ['css', 'scss', 'js', 'jsx', 'ts', 'tsx'],
  tokenFormats: {
    cssVariables: /var\\(--([^)]+)\\)/g,
    scssVariables: /\\$([a-zA-Z0-9-_]+)/g,
    jsTokens: /tokens\\.([a-zA-Z0-9.]+)/g
  }
};
```

### Notification Settings
Configure email and Slack notifications:

```bash
# .env
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@canon.com
SMTP_PASS=your-app-password

SLACK_WEBHOOK_URL=https://hooks.slack.com/services/YOUR/SLACK/WEBHOOK
```

## 📚 API Reference

### Core Endpoints

- `GET /api/dashboard` - Dashboard metrics
- `GET /api/tokens` - Token list with usage data
- `POST /api/scans/run` - Trigger repository scan
- `GET /api/teams` - Team adoption metrics
- `POST /api/change-requests` - Submit change request
- `GET /api/notifications` - User notifications

### WebSocket Events

- `token-change` - Real-time token updates
- `usage-update` - Live usage statistics
- `approval-status` - Change request status updates

## 🧪 Development

### Running Tests
```bash
npm run test
```

### Database Migrations
```bash
cd backend
npx prisma migrate dev --name "migration-name"
```

### Building for Production
```bash
npm run build
```

## 🚀 Deployment

### Environment Setup
1. Set production environment variables
2. Configure database connection
3. Set up email/notification services
4. Configure authentication

### Docker Deployment
```bash
docker-compose up -d
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📋 Roadmap

### Phase 1: Foundation (✅ Complete)
- [x] Basic token scanning
- [x] Simple dashboard
- [x] Email notifications
- [x] Manual approval workflow

### Phase 2: Enhancement (🚧 In Progress)
- [ ] Advanced analytics and reporting
- [ ] Automated impact analysis
- [ ] Smart notification rules
- [ ] Integration with CI/CD pipelines

### Phase 3: Intelligence (📋 Planned)
- [ ] AI-powered usage recommendations
- [ ] Automated deprecation warnings
- [ ] Performance impact analysis
- [ ] Cross-platform token synchronization

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## 🆘 Support

- **Documentation**: [docs/](docs/)
- **Issues**: Create a GitHub issue
- **Email**: design-system@canon.com
- **Slack**: #design-system-support

---

Built with ❤️ by the Canon Design System Team
