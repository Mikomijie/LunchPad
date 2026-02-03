# LunchPad
Validate your startup idea and connect with your entrepreneurial community - all in real-time.
# 🚀 LaunchPad

**Validate your startup idea and connect with your entrepreneurial community - all in real-time.**

Built by **Michael Omijie** for [AI VIBE CODING HACKATHON 2026]

---

## 💡 The Problem

90% of startups fail. Most founders spend months building products nobody wants, working in isolation, missing the events and connections that could have saved them.

## ✨ The Solution

LaunchPad is a dual-purpose platform that helps founders:

1. **Validate ideas instantly** - AI-powered analysis gives you market insights, competition research, and feasibility scores in seconds
2. **Connect with your community** - Discover startup events, pitch nights, and hackathons happening near you RIGHT NOW

## 🎯 Key Features

### AI Startup Validator
- Instant idea analysis using Gemini AI
- Market size estimates and feasibility scoring
- Competitor landscape overview
- Actionable recommendations for next steps
- Related event suggestions

### Real-Time Events Hub
- Browse startup events near your location
- Filter by category (Pitch Nights, Hackathons, Networking, Workshops)
- "Happening Now" live indicators
- Real-time attendee tracking
- Join events and see counts update instantly across all users

### Real-Time Synchronization
- Events appear instantly when created
- Attendee counts sync across all browsers
- Toast notifications for new events
- No refresh needed - everything updates live

**Try it live:** [https://lunchpadd.lovable.app/]

## 🛠️ Tech Stack

- **Frontend:** React + TypeScript
- **Styling:** Tailwind CSS
- **Database:** Supabase (with real-time subscriptions)
- **AI:** Google Gemini API
- **Backend:** Supabase Edge Functions
- **Built with:** Lovable (AI-powered development platform)

## 🏗️ Architecture Highlights

- **Real-time database subscriptions** for instant updates across clients
- **Serverless edge functions** for AI validation with zero cold starts
- **Optimistic UI updates** with React Query for snappy interactions
- **Deduplicated React bundling** to prevent hydration issues


## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or pnpm
- Supabase account (free tier works)

### Installation

```bash
# Clone the repository
git clone https://github.com/[your-username]/launchpad.git
cd launchpad

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Add your Supabase URL and anon key
# Add your Gemini API key

# Run development server
npm run dev
```

### Environment Variables

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_GEMINI_API_KEY=your_gemini_api_key
```

## 📝 Database Schema

```sql
-- Events table with real-time enabled
create table events (
  id uuid primary key default uuid_generate_v4(),
  title text not null,
  description text,
  category text not null,
  location text not null,
  date timestamp with time zone not null,
  attendees integer default 0,
  is_happening_now boolean default false,
  created_at timestamp with time zone default now()
);

-- Enable real-time
alter publication supabase_realtime add table events;
```

## 🎬 3-Minute Pitch

**The Hook:** 90% of startups fail, mostly because they build something nobody wants while isolated from the community that could help them.

**The Solution:** LaunchPad validates your idea in 30 seconds AND connects you with startup events happening near you RIGHT NOW.

**The Demo:**
1. Type in a startup idea → Get instant AI analysis with scores and recommendations
2. Browse events → See pitch nights, hackathons, and networking events near you
3. Real-time magic → Add an event, watch it appear instantly in another browser tab

**The Tech:** React + real-time database + AI validation + serverless edge functions

**The Vision:** Every founder deserves to know if their idea has legs before quitting their job, and they deserve to find their tribe.

## 🏆 Why LaunchPad Wins

1. **Solves a real problem** - Startup validation + community discovery in one place
2. **Technical wow factor** - Real-time synchronization across browsers
3. **AI integration** - Smart, actionable insights powered by Gemini
4. **Practical utility** - Something founders would actually use daily
5. **Execution quality** - Polished UI, smooth animations, production-ready

## 🔮 Future Roadmap

- [ ] User authentication and personalized recommendations
- [ ] Calendar integration for event reminders
- [ ] Community forum for founder discussions
- [ ] Mentor matching based on startup category
- [ ] Integration with actual event APIs (Eventbrite, Meetup)
- [ ] Mobile app (React Native)
- [ ] AI-powered event recommendations based on your idea
- [ ] Pitch deck generator integrated with validation results

## 🤝 Contributing

This was built for a hackathon, but if you'd like to contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

MIT License - feel free to use this project however you'd like!

## 👨‍💻 About the Developer

**Michael Omijie**

Built this entire platform in under 2 hours using modern AI-assisted development tools. LaunchPad demonstrates that with the right tools and vision, one developer can create production-quality applications at lightning speed.

*"Real developers use the best tools available. Speed and execution matter more than doing everything from scratch."*

Connect with me on linkedln [(https://www.linkedin.com/in/michael-omijie-52576328a?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)]

## 🙏 Acknowledgments

- Built with [Lovable](https://lovable.dev) - AI-powered development platform
- AI validation powered by Google Gemini
- Real-time features powered by Supabase
- Design inspiration from modern SaaS applications

---

**⭐ Star this repo if you found it helpful!**

Built with ❤️ and ⚡ by Michael Omijie
