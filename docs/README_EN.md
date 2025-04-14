# Notes - A Modern Note-Taking Application

A modern note-taking application that supports rich text editing, Markdown syntax, real-time preview, and note drag-and-drop sorting functionality.

## Features

- ✨ Rich text editing with Markdown syntax support
- 🔄 Note drag-and-drop sorting
- 💾 Auto-save functionality
- 🎨 Clean and modern interface

## Changelog

For detailed update history, please check:

- CHANGELOG.md (Bilingual)
- CHANGELOG_CN.md (Chinese)
- CHANGELOG_EN.md (English)

## Deployment Guide

For Ubuntu deployment instructions, please check:

- DEPLOY_UBUNTU.md

## How to Run

1. Start backend server:
```bash
python app.py
```

2. Enter the `frontend` directory then start the frontend application:
```bash
cd frontend
npm run dev
```

3. Open browser and visit:
http://localhost:5173

## Technology Stack

### Frontend

- React 18.2.0
- Material-UI (MUI) 5.13.0
- TipTap Editor 2.11.5
- React Beautiful DnD 13.1.1
- Axios 1.4.0
- Vite 4.3.5

### Backend

- Flask 2.0.1
- Flask-CORS 3.0.10
- SQLAlchemy 1.4.23
- Flask-SQLAlchemy 2.5.1
- SQLite

## Installation

### Backend Setup

1. Install Python dependencies:
```bash
pip install -r requirements.txt
```

2. Run Flask server:
```bash
python app.py
```
Server will start at http://127.0.0.1:5000

### Frontend Setup

1. Enter frontend directory:
```bash
cd frontend
```

2. Install Node.js dependencies:
```bash
npm install
```

3. Start development server:
```bash
npm run dev
```
Application will start at http://localhost:5173

## Usage Guide

1. Create note: Click the "+" button in the top right corner
2. Edit note: Input directly in the text area, supporting rich text editing and Markdown syntax
3. Format conversion: Convert notes to different formats (text, headings, lists, quotes, etc.) via right-click menu
4. Sort: Drag notes using the handle on the left to adjust order
5. Delete: Click the delete icon in the top right corner of the note or use the right-click menu

## Development Features

- React Hooks for state management
- TipTap editor integration for rich text editing and Markdown syntax
- Debounce optimization for improved input performance
- RESTful API design
- SQLite data persistence
- Real-time note saving
- Custom drag-and-drop sorting implementation
- Support for multiple note formats (text, headings, lists, quotes, etc.)

## Project Structure

```
Notes/
├── app.py              # Flask backend application
├── config.py           # Configuration file
├── notes.db            # SQLite database file
├── requirements.txt    # Python dependencies
├── CHANGELOG.md        # Bilingual changelog
├── CHANGELOG_CN.md     # Chinese changelog
├── CHANGELOG_EN.md     # English changelog
├── DEPLOY_UBUNTU.md    # Ubuntu deployment guide
├── ERROR_LOG.md        # Error logging
├── models/            # Database models
│   ├── __init__.py    # Package initialization
│   ├── note.py        # Note model
│   └── note_file.py   # Note file model
├── routes/            # API routes
│   ├── __init__.py    # Package initialization
│   ├── notes.py       # Note routes
│   └── files.py       # File routes
├── tests/             # Test directory
│   └── __init__.py    # Test initialization
└── frontend/          # React frontend application
    ├── src/
    │   ├── components/  # React components
    │   ├── hooks/       # Custom hooks
    │   ├── services/    # API services
    │   ├── App.jsx      # Main application component
    │   └── main.jsx     # Application entry
    ├── .env.development # Development environment config
    ├── .env.production  # Production environment config
    ├── package.json     # Node.js dependency configuration
    ├── vite.config.js   # Vite configuration
    └── index.html       # HTML template
```

## Development Plans

### Optimizations

- [x] Optimize adaptive width display of note blocks in the page
- [x] Optimize editing functionality with rich text editing and Markdown syntax
- [ ] Further optimize TipTap editor performance and user experience

### New Features

- [x] Support multiple note formats (text, headings, lists, quotes, etc.)
- [ ] Add note folder creation functionality in the left sidebar
- [ ] Add user authentication system
- [ ] Support note tags and categories
- [ ] Add note search functionality
- [ ] Support image upload and management
- [ ] Add note sharing functionality
- [ ] Support dark mode

## Contribution Guide

Issues and Pull Requests are welcome!

## License

GNU General Public License v3.0