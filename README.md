# 🎓 Leadership Coach

**AI-powered personalized leadership coaching platform for post-workshop continuous improvement.**

A 20-day transformation cycle that helps MBA students practice leadership behaviors, integrate learnings, and receive intelligent feedback grounded in their instructor's teachings.

## Vision

Students attend a 2-day leadership workshop and identify 2-3 development areas. This platform coaches them through a 20-day implementation cycle with:

- **Cognitive psychology-based coaching** (calibration, Socratic challenges, growth mindset)
- **360-degree feedback** from colleagues, managers, and team members
- **Private, safe learning environment** grounded in instructor's content
- **Continuous nudges and check-ins** to maintain momentum
- **Progress tracking and metrics** to measure behavioral change

## Key Features

### Phase 1: Post-Workshop Onboarding
- Student identifies 2-3 development areas
- Links each area to workshop principles
- Creates detailed implementation plans with AI assistance

### Phase 2: 20-Day Implementation Cycle
- **Daily/weekly nudges** personalized to learning style
- **Weekly check-ins** to report progress and obstacles
- **AI coaching feedback** with cognitive psychology techniques:
  - Dunning-Kruger calibration (self-assessment accuracy)
  - Socratic challenges (reveal hidden assumptions)
  - Growth mindset reframing (obstacles as opportunities)
  - Metacognition (learning about learning)
  - Spaced repetition (optimal reinforcement)

### Phase 3: 360-Degree Feedback
- Invite observers (direct reports, peers, manager, mentor)
- Observers report what they actually see
- AI synthesizes: self-perception vs. team observation
- Identify blind spots and celebrate unexpected impacts

### Phase 4: Progress & Integration
- Dashboard shows calibrated progress
- End-of-cycle reflection and next steps
- Optional group coaching sessions
- Accountability partner matching

## Tech Stack

- **Frontend + Backend:** Next.js (App Router)
- **Database:** Supabase (PostgreSQL)
- **Authentication:** Supabase Auth
- **AI/LLM:** LangChain + OpenAI GPT-3.5-turbo
- **Deployment:** Vercel (frontend) + Supabase (backend)
- **Styling:** TailwindCSS

## Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn
- Supabase account (free tier available)
- OpenAI API key

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/ricardodguerra-gif/leadership-coach.git
cd leadership-coach

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env.local

# 4. Add your credentials to .env.local:
# - NEXT_PUBLIC_SUPABASE_URL
# - NEXT_PUBLIC_SUPABASE_ANON_KEY
# - SUPABASE_SERVICE_ROLE_KEY
# - OPENAI_API_KEY

# 5. Set up database
# Run the SQL migrations in supabase/migrations/001_initial_schema.sql
# in your Supabase dashboard

# 6. Run development server
npm run dev

# 7. Open http://localhost:3000
```

See docs/SETUP.md for detailed instructions.

## Project Structure

```
leadership-coach/
├── app/                          # Next.js App Router
│   ├── auth/                     # Authentication pages
│   │   ├── login/
│   │   └── signup/
│   ├── student/                  # Student portal
│   │   ├── dashboard/
│   │   ├── identify-areas/
│   │   ├── create-plan/
│   │   ├── check-in/
│   │   ├── progress/
│   │   └── materials/
│   ├── instructor/               # Instructor portal
│   │   ├── dashboard/
│   │   ├── upload-materials/
│   │   └── analytics/
│   ├── observer/                 # 360-degree feedback
│   │   └── feedback/
│   ├── api/                      # API routes
│   │   ├── auth/
│   │   ├── coaching/
│   │   └── feedback/
│   └── layout.tsx
├── lib/                          # Utilities and business logic
│   ├── agents/                   # AI coaching engine
│   │   ├── coaching-engine.ts
│   │   ├── calibration.ts
│   │   ├── socratic-challenge.ts
│   │   ├── metacognition.ts
│   │   ├── growth-mindset.ts
│   │   └── feedback-synthesis.ts
│   ├── supabase.ts              # Supabase client
│   └── utils/
├── supabase/
│   └── migrations/
│       └── 001_initial_schema.sql
├── docs/                         # Documentation
│   ├── ARCHITECTURE.md
│   ├── DATABASE_SCHEMA.md
│   ├── COACHING_STRATEGIES.md
│   ├── IMPLEMENTATION_PLAN.md
│   ├── SETUP.md
│   └── API.md
├── .env.example
├── .gitignore
├── package.json
├── tsconfig.json
└── tailwind.config.js
```

## Development Roadmap

### Week 1-2: Foundation & MVP
- [ ] Project setup and authentication
- [ ] Database schema and initial migration
- [ ] Student dashboard and development area identification
- [ ] Plan creation with AI assistance
- [ ] Basic coaching engine (calibration, Socratic, growth mindset)

### Week 3-4: Check-ins & Feedback Loop
- [ ] Weekly check-in form
- [ ] AI feedback generation
- [ ] Feedback history and tracking
- [ ] Progress dashboard
- [ ] Self-assessment surveys

### Week 5-6: 360-Degree Feedback
- [ ] Observer invitation system
- [ ] Observer feedback collection
- [ ] Feedback synthesis (self vs. team)
- [ ] Blind spot identification

### Week 7-8: Advanced Features
- [ ] Nudge generation and scheduling
- [ ] Spaced repetition system
- [ ] Instructor content management
- [ ] Analytics and reporting
- [ ] Group coaching features

### Week 9+: Polish & Launch
- [ ] User testing with pilot group
- [ ] Security audit and RLS policies
- [ ] Performance optimization
- [ ] Documentation
- [ ] Production deployment

## Key Design Principles

1. **Grounded in Your Teaching** - Every feedback references course material
2. **Evidence-Based** - Students report what they actually did and observed
3. **Safe & Private** - All reflections are confidential unless explicitly shared
4. **Psychologically Informed** - Uses cognitive psychology research
5. **Behavior-Focused** - Goal is changed behavior, not completed forms
6. **Adaptive** - Feedback adapts to learning style and progress
7. **Iterative** - Students can refine plans based on feedback

## Cognitive Psychology Elements

The coaching engine integrates:

- **Dunning-Kruger Calibration** - Help students see their performance objectively
- **Socratic Challenges** - Gentle questions reveal hidden assumptions
- **Growth Mindset** - Reframe obstacles as learning opportunities
- **Metacognition** - Teach students to learn from any experience
- **Social Learning** - Provide modeling and examples
- **Spaced Repetition** - Reinforce concepts at optimal intervals
- **Cognitive Load Management** - Progressive complexity, not overwhelm

## License

MIT License

## Contact

For questions about the project:
- Ricardo Guerra (Project lead)
- GitHub Issues for bug reports and feature requests

---

**Status:** 🚀 Active Development - Week 1-2 Sprint
