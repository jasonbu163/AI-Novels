# AGENTS.md

Guidelines for AI agents working in this AI-assisted Chinese novel writing repository.

## Project Overview

This is an AI-assisted Chinese novel creation project using the `chinese-novelist` skill. The completed novel "暗影秘史" (Shadow Secret History) is a 15-chapter fantasy novel totaling 58,513 words.

**Current Status:**
- Novel: 暗影秘史 (Fantasy genre, 15 chapters, 100% complete)
- Total word count: 58,513 words
- Average per chapter: 3,901 words

## Available Commands

### Word Count Verification

Check chapter word counts using the skill script:

```bash
# Check single chapter
python /Users/jason/.config/opencode/skills/chinese-novelist-skill/scripts/check_chapter_wordcount.py novels/暗影秘史/第01章-暗夜密约.md

# Check all chapters in directory
python /Users/jason/.config/opencode/skills/chinese-novelist-skill/scripts/check_chapter_wordcount.py --all novels/暗影秘史/

# Custom minimum word count
python /Users/jason/.config/opencode/skills/chinese-novelist-skill/scripts/check_chapter_wordcount.py novels/暗影秘史/第01章-暗夜密约.md 3500
```

### Novel Status

```bash
# View outline and progress
cat novels/暗影秘史/00-大纲.md

# View character profiles
cat novels/暗影秘史/01-人物档案.md

# List all chapters
ls novels/暗影秘史/
```

## File Structure

```
novels/
└── [novel-name]/
    ├── 00-大纲.md          # Master outline with TODO list
    ├── 01-人物档案.md       # Character profiles
    ├── 第01章-[title].md   # Chapter files
    ├── 第02章-[title].md
    └── ...
```

### Naming Conventions

- **Outline**: `00-大纲.md`
- **Characters**: `01-人物档案.md`
- **Chapters**: `第[NN]章-[title].md` (e.g., `第01章-暗夜密约.md`)
- Use Chinese numerals with leading zeros for chapter numbers

## Content Guidelines

### Three Golden Rules

1. **Show, Don't Tell** - Use actions and dialogue, avoid direct statements
2. **Conflict-Driven Plot** - Every chapter must have conflict or twists
3. **Cliffhanger Endings** - Every chapter must end with a hook

### Writing Standards

**Chapter Requirements:**
- Target: 3,000-5,000 words per chapter
- Minimum: 3,000 words (rewrite if below)
- Structure: 3-5 scenes per chapter
- Hook: First 20% must have immediate conflict

**Style Guidelines:**
- Remove AI clichés: "璀璨", "瑰丽", "绚烂" (avoid flowery AI堆砌)
- Replace abstract emotions with concrete actions/dialogue
- Avoid four-character clichés: "心潮澎湃", "热血沸腾"
- Dialogues should be personalized, avoid formal written language
- Alternate long and short sentences for rhythm
- Use specific sensory details (visual/auditory/olfactory)

### Outline Format (00-大纲.md)

Must include:
- Basic info: genre, chapter count, target word count, core conflict
- TODO list with checkboxes for each chapter
- Chapter planning table with: chapter, title, core event, hook, word count, status
- Book-wide suspense arcs (main/sub/ultimate revelations)
- Word count statistics
- Chapter summaries (300-500 words each)

### Character Profile Format (01-人物档案.md)

For each character include:
- Name, age, occupation
- Physical appearance
- Core personality
- Values, greatest fear, fatal flaw
- Inner desire, backstory
- MBTI type

## Workflow for New Novels

To start a new novel, load the `chinese-novelist` skill:

```bash
# The skill provides 3-phase workflow:
# Phase 1: 5-question confirmation (genre, protagonist, personality, conflict, chapters)
# Phase 2: Planning + secondary confirmation (outline + character profiles)
# Phase 3: Auto-creation (chapter by chapter without further confirmation)
```

### Per-Chapter Creation Process

1. **Pre-writing Analysis**
   - Read `00-大纲.md` for TODO and previous chapter summaries
   - Update TODO to mark current chapter "in progress"
   - Design opening hook (first 20% must have immediate conflict)
   - Plan 3-5 scenes

2. **Writing**
   - Create chapter file using template
   - Write 3,000-5,000 words
   - Set ending hook
   - Verify word count with script

3. **Post-writing Optimization**
   - Check consistency (characters, plot, pacing)
   - Deep polish: remove AI痕迹 per style guidelines
   - Re-check word count (must be ≥3000)

4. **Finalization**
   - Add chapter summary (300-500 words) to outline
   - Update TODO to mark chapter "complete"

## Quality Checklist

Before considering a chapter complete:
- [ ] Word count ≥ 3,000 (verified by script)
- [ ] Opening has immediate conflict
- [ ] Contains 3-5 scenes
- [ ] Ends with cliffhanger hook
- [ ] AI痕迹 removed (no clichés, abstract emotions, or堆砌)
- [ ] Consistent with previous chapters
- [ ] Summary added to outline
- [ ] TODO list updated

## Reference Materials

Skill references available at:
`/Users/jason/.config/opencode/skills/chinese-novelist-skill/references/`

- `chapter-guide.md` - Chapter structure & opening techniques
- `hook-techniques.md` - 10 types of ending hooks
- `dialogue-writing.md` - Dialogue standards
- `character-building.md` - Character development
- `content-expansion.md` - 7 expansion techniques
- `consistency.md` - Consistency guidelines
- `quality-checklist.md` - Pre-delivery checklist
