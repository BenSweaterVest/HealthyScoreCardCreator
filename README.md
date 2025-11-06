# Health Scorecard Creator

**Live Tool:** https://healthyscorecardcreator.pages.dev/

Build your own custom health scorecard in minutes. No coding needed - just fill in your goals, define your scoring, and download a ready-to-use HTML file.

**Related Project:** [HealthyScoreCard](https://github.com/BenSweaterVest/HealthyScoreCard) - My personal scorecard that inspired this tool

## What This Does

Create your own custom health scorecard by:

1. **Setting 5 health goals** - Whatever you want to track (sleep, nutrition, exercise, mindfulness, etc.)
2. **Defining your scoring** - Set what earns 0, 1, or 2 points for each goal
3. **Downloading your scorecard** - Get a fully functional HTML file you can use immediately

Your generated scorecard includes:
- Clickable scoring with visual feedback
- Name fields for evaluator and client
- Weekly check-in questions and notes
- Copy-to-clipboard functionality
- Reset button for fresh starts
- Clean, professional design
- Works great on mobile

## Why I Built This

I made the [original Health Scorecard](https://github.com/BenSweaterVest/HealthyScoreCard) for my own health goals, and it worked great. But every time someone asked "can I use this for MY goals?" I had to say "sure, just edit the HTML and JavaScript..."

That sucked. So I built this creator.

Now dietitians, coaches, trainers, therapists, or anyone tracking goals can make their own customized scorecard without touching code.

## How to Use It

1. **Go to** https://healthyscorecardcreator.pages.dev/
2. **Set your scorecard title** (like "Weekly Fitness Goals" or "Monthly Wellness Check")
3. **Fill in your 5 goals:**
   - Goal title (like "Hydration" or "Sleep Quality")
   - Target description (like "8 glasses of water daily")
   - Scoring criteria:
     - Score 2: Crushed it
     - Score 1: Good effort
     - Score 0: Needs work
4. **Click "Download index.html"** to get your scorecard
5. **Use it:**
   - Open the file in any browser
   - Fill it out weekly or monthly
   - Copy results to share with clients, coaches, or keep for yourself

## Who's This For?

### Dietitians
Build different scorecards for different clients:
- Weight loss tracking (meals, exercise, food logging)
- Diabetes management (blood sugar checks, meds, diet adherence)
- Sports nutrition (pre/post workout meals, hydration, supplements)

### Fitness Coaches
Track what actually matters:
- Workout attendance and effort
- Recovery habits (sleep, stretching, rest days)
- Nutrition consistency

### Mental Health Professionals
Monitor wellness practices:
- Meditation/mindfulness
- Sleep quality
- Social connections
- Stress management
- Homework completion

### Anyone Else
Track literally anything with a scoring system:
- Academic goals (study time, assignments, attendance)
- Professional development (skill practice, networking, reading)
- Creative projects (daily practice, sharing work, learning)

## Technical Stuff

### What You Get

The creator spits out a complete, standalone HTML file with everything built in:

- **CSS styling** - Looks professional, works on mobile
- **JavaScript** - Click handling, score tracking, form management
- **Clipboard integration** - One-click copy with fallback
- **Reset button** - Fresh start each week
- **Results preview** - See output before copying

Everything in ONE file. No external dependencies, no server needed, works offline.

### Why Single Files Rock

Both the creator and generated scorecards are single HTML files:
- Zero installation
- Works on any device with a browser
- No internet needed after download
- Share via email, Dropbox, whatever
- Complete privacy - nothing sent anywhere

### Browser Support

Works everywhere modern:
- Chrome/Edge (best experience)
- Firefox
- Safari
- Mobile browsers (iOS Safari, Android Chrome)

## Deploy Your Own

I host this on Cloudflare Pages (it's free and stupid easy):

1. **Fork this repo** on GitHub
2. **Connect to Cloudflare Pages:**
   - Go to [pages.cloudflare.com](https://pages.cloudflare.com)
   - Login with GitHub
   - "Create a project" → "Connect to Git"
   - Pick your fork
   - Leave everything default
   - "Save and Deploy"
3. **Done** - Your creator is live at `yourprojectname.pages.dev`

Pushes to main auto-deploy in ~30 seconds.

### Other Options

- **GitHub Pages:** Repo settings → Pages → Source: main branch
- **Netlify:** Drag and drop `index.html`
- **Any web server:** Just upload `index.html`

## Want to Customize It?

Feel free to fork and modify:

### More/Fewer Goals
Currently locked at 5 goals. To change:
1. Add/remove goal sections in the HTML
2. Update `buildHTML()` function for the new count
3. Update form field IDs

### Different Scoring
Currently 0-2 points. To change:
1. Update score input fields
2. Modify generated JavaScript for new ranges
3. Update maxScores calculation

### Different Look
All styles are in `index.html`:
1. Creator form styles in `<style>` tag
2. Generated scorecard styles in `buildHTML()` function

## What the Output Looks Like

The "Copy Results" button gives you clean, formatted text:

```
WEEKLY GOALS
=======
Evaluator: Coach Sarah
Patient: Alex Johnson

Hydration: 2 / 2
Sleep Quality: 1 / 2
Exercise Consistency: 2 / 2
Meal Prep: 2 / 2
Mindfulness Practice: 1 / 2

**Total Score: 8 / 10**

Quick Weekly Check-In:

Biggest win: Hit all hydration goals this week
Main challenge: Sleep schedule was inconsistent
What helped: Setting phone reminders for water
Next week focus: Earlier bedtime routine
Dietitian Notes: Excellent progress on hydration. Work on sleep consistency.
```

Perfect for:
- Messaging apps
- Client notes
- Email updates
- Tracking spreadsheets

## Maybe Someday

Ideas I might add:
- **Variable goal count** - Pick 3-10 goals instead of fixed 5
- **Flexible scoring** - Support 0-3 or 0-5 scales
- **Templates** - Pre-built setups for common uses
- **Color themes** - Customize the look
- **Batch download** - Generate multiple scorecards at once
- **Save/load settings** - Keep your configurations
- **Preview mode** - Test before downloading

## How This Relates to HealthyScoreCard

This generates scorecards like [HealthyScoreCard](https://github.com/BenSweaterVest/HealthyScoreCard).

Think of it like:
- **HealthyScoreCard** = My personal scorecard
- **HealthyScoreCardCreator** = This tool (makes custom scorecards)

## Contributing

Bug? Idea? Open an issue or PR.

Core philosophy: **Keep it simple and self-contained.** No external dependencies, no backend, no complex setup.

## License

MIT - do whatever you want with it.

## Questions?

- Open a GitHub issue
- Check [HealthyScoreCard](https://github.com/BenSweaterVest/HealthyScoreCard) for examples
- See customization sections above

---

Built for anyone who tracks goals and wants to measure progress.
