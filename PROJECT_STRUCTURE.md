# Project Structure

This document describes the organized structure of the µLM AI Playground project.

## Root Directory

```
MuLM/
├── src/                    # Source code
├── docs/                   # Documentation
├── scripts/                # Build and setup scripts
├── test/                   # Test files
├── dist/                   # Build output (generated)
├── node_modules/           # Dependencies (generated)
├── index.html              # Entry HTML file
├── package.json            # Project dependencies and scripts
├── tsconfig.json           # TypeScript configuration
├── vite.config.ts          # Vite build configuration
├── tailwind.config.js      # Tailwind CSS configuration
├── postcss.config.js       # PostCSS configuration
├── .eslintrc.cjs           # ESLint configuration
├── .gitignore              # Git ignore rules
├── .env.example            # Environment variables template
├── README.md               # Main project documentation
├── LICENSE                 # MIT License
└── CONTRIBUTING.md         # Contribution guidelines
```

## Source Directory (`src/`)

```
src/
├── main.tsx                # Application entry point
├── App.tsx                 # Main React component with routing
├── index.css               # Global styles
├── vite-env.d.ts           # Vite type definitions
├── components/             # Reusable UI components
│   ├── assistant/          # AI assistant components
│   ├── editor/             # Code editor components
│   ├── export/             # Export functionality
│   └── workspace/          # Workspace UI components
├── pages/                  # Page components (routes)
├── services/               # Business logic and API services
├── storage/                # Local storage utilities
├── execution/              # Workflow execution engine
├── export/                 # Export system
├── simulation/             # Workflow simulation
├── types/                  # TypeScript type definitions
├── styles/                 # Additional stylesheets
├── data/                   # Static data and examples
└── demo/                   # Demo-specific code
```

## Documentation Directory (`docs/`)

```
docs/
├── API_REFERENCE.md                # API documentation
├── DEPLOYMENT_GUIDE.md             # Deployment instructions
├── AI_BLOCK_GENERATOR.md           # AI block generation guide
├── OPENAI_INTEGRATION.md           # OpenAI setup guide
├── UNIVERSAL_EXPORT_SYSTEM.md      # Export system documentation
├── HACKATHON_PRESENTATION.md       # Presentation guide
├── GITHUB_SETUP_GUIDE.md           # GitHub setup instructions
├── TROUBLESHOOTING_GUIDE.md        # Common issues and solutions
├── DRAG_DROP_GUIDE.md              # Drag & drop usage guide
├── DEMO.md                         # Demo instructions
├── DEMO_SCRIPT.md                  # Demo script
├── HACKATHON_SUBMISSION.md         # Hackathon submission info
└── archive/                        # Archived documentation
```

## Scripts Directory (`scripts/`)

```
scripts/
├── setup.sh                # Initial project setup
└── build.sh                # Production build script
```

## Key Configuration Files

### package.json
Contains all project dependencies, scripts, and metadata.

**Main Scripts:**
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run type-check` - TypeScript type checking

### tsconfig.json
TypeScript compiler configuration with strict type checking enabled.

### vite.config.ts
Vite bundler configuration for fast development and optimized builds.

### tailwind.config.js
Tailwind CSS configuration with custom theme and plugins.

## Environment Variables

Copy `.env.example` to `.env` and configure:

```env
VITE_OPENAI_API_KEY=your_api_key_here
VITE_API_BASE_URL=http://localhost:3000
```

## Build Output

The `dist/` directory contains the production build:
- Optimized JavaScript bundles
- Compiled CSS
- Static assets
- index.html

## Development Workflow

1. **Install dependencies**: `npm install`
2. **Start dev server**: `npm run dev`
3. **Make changes**: Edit files in `src/`
4. **Type check**: `npm run type-check`
5. **Lint**: `npm run lint`
6. **Build**: `npm run build`
7. **Preview**: `npm run preview`

## Notes

- TypeScript errors related to unused imports are warnings and don't affect functionality
- The project uses React 18 with TypeScript
- Styling is done with Tailwind CSS and custom CSS
- Framer Motion provides smooth animations
- React Flow handles the visual workflow canvas
