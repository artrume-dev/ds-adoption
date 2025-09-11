<!-- Use this file to provide workspace-specific custom instructions to Copilot. For more details, visit https://code.visualstudio.com/docs/copilot/copilot-customization#_use-a-githubcopilotinstructionsmd-file -->
- [x] Verify that the copilot-instructions.md file in the .github directory is created.

- [x] Clarify Project Requirements
	<!-- Design Tokens usage tracker dashboard with React frontend, Node.js backend, PostgreSQL database, and WebSocket real-time updates -->

- [x] Scaffold the Project
	<!-- Created full-stack project structure with frontend, backend, and database components -->

- [x] Customize the Project
	<!-- Implemented token scanner, dashboard, notifications, and approval workflow with basic UI components -->

- [x] Install Required Extensions
	<!-- No specific extensions required -->

- [x] Compile the Project
	<!-- Installed dependencies and verified frontend compilation -->

- [x] Create and Run Task
	<!-- Created development task for running frontend and backend concurrently -->

- [x] Launch the Project
	<!-- Frontend launched successfully on http://localhost:3001 -->

- [x] Ensure Documentation is Complete
	<!-- README.md created with comprehensive project information and setup instructions -->

## Project Requirements
This is a Design Tokens usage tracker dashboard system with:

### Core Features:
1. Track which teams and digital channels use design tokens
2. Monitor design token usage across websites and apps  
3. Track pattern usage from Canon Design System
4. Display token dependencies and usage metrics
5. Show design system contributor information
6. Send notifications for token value updates
7. Provide review and approval workflow for changes
8. Enable test environment deployment before production

### MVP Features (High-impact, Low-effort):
- Basic token usage scanner
- Simple dashboard showing top used tokens
- Email notifications for major changes
- Manual approval workflow

### Tech Stack:
- Frontend: React with data visualization (D3.js, Chart.js)
- Backend: Node.js with REST APIs
- Database: PostgreSQL for relational data, Redis for caching
- Real-time: WebSocket connections for live updates
