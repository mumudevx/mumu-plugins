<p align="center">
  <strong>FitForge</strong> — Claude Code Plugin
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue" alt="version" />
  <img src="https://img.shields.io/badge/license-MIT-green" alt="license" />
  <img src="https://img.shields.io/badge/claude--code-plugin-purple" alt="claude code plugin" />
</p>

<p align="center">
  🇬🇧 English | <a href="README_tr.md">🇹🇷 Türkçe</a>
</p>

---

Personalized fitness & nutrition program generator powered by two AI expert agents. Produces a complete weekly training + meal plan tailored to your body metrics and goals.

## How It Works

1. You describe your body stats, equipment, and goals as free text
2. **Marcus Reid** (PT Agent) — generates a science-based weekly training program
3. **Dr. Elena Vasquez** (Nutrition Agent) — builds a nutrition plan synchronized with training load
4. The orchestrator combines both plans into a unified report

Both agents can cite peer-reviewed research via WebSearch (PubMed, JISSN, JSCR, Sports Medicine).

## Installation

Via mumu-plugins marketplace:

```bash
claude plugin add https://github.com/mumudevx/mumu-plugins.git
```

## Usage

### Generate a Full Program

```
/fitforge:start --lang en I'm 28 years old, male, 180cm, 85kg, moderately active, have full gym access, goal is muscle gain
```

The `--lang` flag sets the output language (ISO 639-1 code). Default is `tr` (Turkish). Examples: `en`, `de`, `fr`, `es`, `ar`, `ja`.

### Use a Starter Prompt File

Prepare your body data in a markdown file and reference it directly:

```
/fitforge:start --lang en @starter-prompt-example.md
```

See `starter-prompt-example.md` for the expected format.

### Ask the PT a Question

```
/fitforge:ask-marcus --lang en What's the best rep range for hypertrophy?
```

Marcus Reid answers questions about training principles, exercise form, progressive overload, injury prevention, and program modifications.

### Ask the Nutritionist a Question

```
/fitforge:ask-elena --lang en How much protein should I eat post-workout?
```

Dr. Elena Vasquez answers questions about nutrition science, macros, supplements, meal timing, hydration, and diet modifications.

## Components

| Component | Type | Description |
|-----------|------|-------------|
| `fitforge` | Skill | Main orchestrator workflow |
| `marcus-reid` | Agent | PT — training program generation |
| `dr-elena-vasquez` | Agent | Nutritionist — meal plan generation |
| `/fitforge:start` | Command | Generate full weekly program |
| `/fitforge:ask-marcus` | Command | Q&A with PT agent |
| `/fitforge:ask-elena` | Command | Q&A with nutrition agent |

## License

MIT
