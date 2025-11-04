# Health Scorecard Creator

A web-based tool for creating customized health scorecard generators. This is the creator tool that generates the interactive scorecards you can see at [healthyscorecard.pages.dev](https://healthyscorecard.pages.dev/).

**Live Creator Tool:** https://healthyscorecardcreator.pages.dev/

**Related Project:** [HealthyScoreCard](https://github.com/BenSweaterVest/HealthyScoreCard) - The reference scorecard implementation

## What it does

This tool lets you create custom health scorecards by:

1. **Defining your own goals** - Set 5 custom health goals with titles and descriptions
2. **Customizing scoring criteria** - Define what earns 0, 1, or 2 points for each goal
3. **Generating a standalone HTML file** - Download a fully functional, interactive scorecard

The generated scorecard is a complete, self-contained HTML file with:
- Clickable score selection with visual feedback
- Name fields for evaluator and patient/client
- Weekly check-in questions and notes
- Copy to clipboard functionality
- Form reset capability
- Professional styling
- Mobile-responsive design

## Why I built this

The [original Health Scorecard](https://github.com/BenSweaterVest/HealthyScoreCard) works great for my specific health goals, but I wanted to make it easy for anyone to create their own customized version without editing HTML or JavaScript.

This creator tool lets dietitians, health coaches, fitness trainers, therapists, or anyone tracking goals create their own scorecard in minutes - no coding required.

## How to use it

1. **Open the creator** at https://healthyscorecardcreator.pages.dev/
2. **Set your scorecard title** (e.g., "Weekly Fitness Goals", "Monthly Wellness Check")
3. **For each of the 5 goals:**
   - Enter the goal title (e.g., "Hydration", "Sleep Quality")
   - Add a target description (e.g., "8 glasses of water daily")
   - Define scoring criteria:
     - Score 2: Excellent performance
     - Score 1: Good effort
     - Score 0: Needs improvement
4. **Click "Download index.html"** to get your custom scorecard
5. **Use your scorecard:**
   - Open the downloaded file in any browser
   - Fill it out weekly/monthly
   - Copy results to share with clients, coaches, or for personal tracking

## Example Use Cases

### For Dietitians
Create scorecards for different client types:
- Weight loss program (nutrition adherence, exercise, meal logging)
- Diabetes management (blood sugar testing, medication compliance, dietary guidelines)
- Sports nutrition (pre/post workout meals, hydration, supplement timing)

### For Fitness Coaches
Track client progress on:
- Workout attendance and intensity
- Recovery practices (sleep, stretching, rest days)
- Nutrition habits aligned with fitness goals

### For Mental Health
Monitor wellness activities:
- Meditation/mindfulness practice
- Sleep hygiene
- Social connections
- Stress management techniques
- Therapy homework completion

### For Personal Use
Create your own accountability system for any area:
- Academic goals (study time, assignment completion, attendance)
- Professional development (skill practice, networking, reading)
- Creative projects (daily practice, sharing work, learning new techniques)

## Technical Details

### What gets generated

The creator builds a complete, standalone HTML file that includes:

- **Full CSS styling** - Professional, mobile-responsive design
- **Interactive JavaScript** - Click handlers, score tracking, form management
- **Data attributes** - Proper DOM structure for score selection
- **Clipboard API integration** - One-click copy to clipboard with fallback
- **Form reset functionality** - Start fresh each week
- **Results preview** - See formatted output before copying

All of this in a single HTML file - no external dependencies, no server required, works offline.

### Self-contained files

Both the creator and the generated scorecards are single HTML files. This means:
- No installation needed
- Works on any device with a browser
- No internet required after downloading
- Easy to share via email or file sharing
- Complete privacy - nothing sent to servers

### Browser compatibility

Works in all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Mobile browsers (iOS Safari, Chrome on Android)

## Deployment

This project is hosted on Cloudflare Pages:

1. **Fork this repository** on GitHub
2. **Connect to Cloudflare Pages:**
   - Go to [pages.cloudflare.com](https://pages.cloudflare.com)
   - Sign up/login with GitHub
   - Click "Create a project" → "Connect to Git"
   - Select your fork
   - Leave all settings as default (static HTML)
   - Click "Save and Deploy"
3. **Your creator will be live** at `yourprojectname.pages.dev`

Every push to the main branch automatically redeploys in about 30 seconds.

### Alternative Deployment Options

- **GitHub Pages:** Enable in repo settings → Pages → Source: main branch
- **Netlify:** Drag and drop the `index.html` file
- **Any web server:** Just upload `index.html` - it's that simple

## Customizing the Creator

If you want to modify the creator tool itself:

### Change the number of goals
Currently supports 5 goals. To add more:
1. Add new goal sections in the HTML form
2. Update the `buildHTML()` function to generate the additional goals
3. Add corresponding form field IDs

### Modify the scoring scale
Currently uses 0-2 points. To change:
1. Update the score input fields in the creator form
2. Modify the generated JavaScript to handle different score ranges
3. Update the maxScores calculation in the generated code

### Change styling
All styles are in the `index.html` file:
1. Creator UI styles in the `<style>` tag - controls how the creator form looks
2. Generated scorecard styles in the `buildHTML()` function - controls how the output scorecard looks

## Output Format

When users click "Copy Results" in a generated scorecard, they get nicely formatted text:

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

This format works great for:
- Pasting into messaging apps
- Adding to client notes
- Email updates
- Progress tracking spreadsheets

## Future Ideas

Potential enhancements:
- **Variable goal count** - Choose 3-10 goals instead of fixed 5
- **Flexible scoring** - Support 0-3 or 0-5 point scales
- **Goal templates** - Pre-built templates for common use cases
- **Color themes** - Let users customize the appearance
- **Multi-scorecard download** - Generate multiple variations at once
- **Import/Export settings** - Save your creator configurations
- **Preview mode** - Test the scorecard before downloading

## Relationship to HealthyScoreCard

This project generates scorecards like the one in [BenSweaterVest/HealthyScoreCard](https://github.com/BenSweaterVest/HealthyScoreCard).

- **HealthyScoreCard** = A specific scorecard for my personal health goals
- **HealthyScoreCardCreator** = Tool to create your own custom scorecards

Think of it like:
- HealthyScoreCard is a specific resume
- HealthyScoreCardCreator is a resume builder

## Contributing

Found a bug or have an idea? Open an issue or submit a pull request.

Keep in mind the core philosophy: **simplicity and self-contained functionality**. Features should not require external dependencies, backend services, or complex setup.

## License

MIT License - use it however you want. See LICENSE file for details.

## Support

For issues or questions:
- Open an issue on GitHub
- Check the [HealthyScoreCard repo](https://github.com/BenSweaterVest/HealthyScoreCard) for usage examples
- For questions about customization, see the "Customizing" sections above

---

Built for anyone tracking goals and wanting to measure progress.
