# Quick Start Guide

Welcome! This guide will help you quickly add a new topic to the knowledge base.

## 5-Minute Setup

### 1. Choose Your Category
- `topics/applications/` - Apps and platforms (e.g., Coolify, WordPress)
- `topics/frameworks/` - Dev frameworks (e.g., React, Django)
- `topics/tools/` - Developer tools (e.g., Docker, Git)
- `topics/languages/` - Programming languages (e.g., Python, Rust)

### 2. Create Your Topic
```bash
# Replace <category> and <topic-name> with your choices
cd topics/<category>
mkdir <topic-name>
cp ../../.templates/topic-template.md <topic-name>/README.md
```

### 3. Fill in the Template
Edit `<topic-name>/README.md` with:
- Brief overview (2-3 sentences)
- Key features (bullet points)
- Installation instructions
- Common use cases
- Links to official docs

### 4. Update the Index
Add your topic to:
1. Main `README.md` (under appropriate category)
2. `INDEX.md` (alphabetically organized)
3. Category `README.md` (in `topics/<category>/`)

### 5. Submit Your Contribution
```bash
git add .
git commit -m "Add <topic-name> to <category>"
git push
```

## What Makes a Good Entry?

✅ **DO:**
- Test all commands before including them
- Link to official documentation
- Use clear, concise language
- Follow the template structure
- Include practical examples

❌ **DON'T:**
- Copy-paste from other sources without verification
- Include personal opinions
- Use marketing language
- Leave sections empty (use "N/A" if not applicable)

## Example Structure

```
topics/tools/docker/
├── README.md           # Main documentation
├── examples/           # Optional: code examples
│   ├── simple-app/
│   └── multi-container/
└── configs/           # Optional: config files
    └── docker-compose.yml
```

## Need Help?

- Check existing topics for examples
- Read [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines
- Look at the [template](.templates/topic-template.md)
- Open an issue if you have questions

## Quality Checklist

Before submitting:
- [ ] All code examples tested
- [ ] Links verified and working
- [ ] Spelling and grammar checked
- [ ] README.md and INDEX.md updated
- [ ] Follows template structure
- [ ] Includes cross-references to related topics

---

Happy contributing! 🚀
