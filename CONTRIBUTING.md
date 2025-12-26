# Contributing Guidelines

Thank you for considering contributing to the Knowledge Base for LLMs! This document provides guidelines for adding and maintaining content.

## How to Contribute

### Adding a New Topic

1. **Choose the Right Category**
   - `topics/applications/` - Software applications and platforms
   - `topics/frameworks/` - Development frameworks
   - `topics/tools/` - Developer tools and utilities
   - `topics/languages/` - Programming languages

2. **Create Topic Directory**
   ```bash
   mkdir -p topics/<category>/<topic-name>
   ```

3. **Use the Template**
   ```bash
   cp .templates/topic-template.md topics/<category>/<topic-name>/README.md
   ```

4. **Fill in the Content**
   - Use the template sections as a guide
   - Be concise and factual
   - Include practical examples
   - Verify all commands and code snippets

5. **Update Documentation**
   - Add your topic to the main `README.md`
   - Update `INDEX.md` with your entry
   - Include cross-references to related topics

### Content Standards

#### Writing Style
- **Clear and concise**: Avoid unnecessary jargon
- **Objective**: Stick to facts, not opinions
- **Practical**: Include real-world examples
- **Structured**: Follow the template format
- **Current**: Use up-to-date information

#### Technical Accuracy
- Test all code examples and commands
- Verify installation instructions
- Include version numbers where relevant
- Link to official documentation
- Cite sources for technical claims

#### Formatting
- Use Markdown consistently
- Follow existing formatting patterns
- Use code blocks with language identifiers
- Include proper heading hierarchy
- Add blank lines for readability

### What to Include

#### Essential Sections
Every topic must have:
1. **Overview** - 2-3 sentence introduction
2. **Key Features** - Bullet points of main capabilities
3. **Use Cases** - When to use this technology
4. **Installation/Setup** - Getting started guide
5. **Resources** - Official links and documentation

#### Optional Sections
Include if relevant:
- Requirements/Prerequisites
- Common Commands/Usage
- Architecture/How it Works
- Best Practices
- Common Pitfalls
- Configuration examples
- Troubleshooting tips

### What NOT to Include

- Personal opinions or bias
- Marketing language or hype
- Outdated information
- Unverified claims
- Copied content without attribution
- Sensitive information or credentials

## Review Process

### Before Submitting
- [ ] Content follows the template structure
- [ ] All code examples are tested
- [ ] Links are valid and point to official sources
- [ ] Spelling and grammar are correct
- [ ] Topic is added to README.md and INDEX.md
- [ ] Related topics are cross-referenced

### Pull Request Guidelines
- Use a descriptive title: "Add [topic-name] to [category]"
- Describe what you're adding and why it's valuable
- Mention any related topics or dependencies
- Keep changes focused on one topic per PR

## Topic Organization

### Directory Structure
```
topics/<category>/<topic-name>/
├── README.md          # Main topic content (required)
├── examples/          # Code examples (optional)
├── configs/           # Configuration files (optional)
└── assets/            # Images or diagrams (optional)
```

### Naming Conventions
- Use lowercase for directory names
- Use hyphens for multi-word names
- Be descriptive but concise
- Match common/official naming when possible

Examples:
- ✅ `coolify` (single word)
- ✅ `visual-studio-code` (multi-word)
- ✅ `react-native` (official name)
- ❌ `VSCode` (use hyphens, not camelCase)
- ❌ `my-cool-app` (too generic)

## Updating Existing Content

### When to Update
- Technology has new major features
- Installation process has changed
- Links are broken or outdated
- Information is inaccurate
- Better examples are available

### How to Update
1. Make targeted changes to specific sections
2. Update version numbers if relevant
3. Test any changed commands or code
4. Note what changed in your PR description
5. Update the last-updated date if present

## Questions or Help

If you're unsure about:
- Which category to use
- How to structure complex information
- Whether content is appropriate
- Technical accuracy

Please open an issue to discuss before submitting a PR.

## Code of Conduct

- Be respectful and constructive
- Focus on improving the knowledge base
- Give credit where credit is due
- Help maintain quality standards
- Welcome newcomers and their contributions

---

Thank you for helping build a comprehensive knowledge base for LLMs!
