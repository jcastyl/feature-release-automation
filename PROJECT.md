# Project Documentation

## Feature Release Documentation Standards

This project follows standardized feature release documentation as outlined in the Notion page "Feature release: specifications".

### Template Structure

All feature release documents should follow this structure:

1. **1-Minute Summary** - 2-3 key highlights with user impact
2. **Feature Updates** - Detailed breakdown of new features with:
   - What's new (brief description)
   - Impact (why it matters/workflow improvement)
   - How it works (step-by-step process)
3. **Behind the Scenes** - Technical improvements including:
   - Reliability improvements
   - System/Performance updates
4. **Growth Spotlight** - Community highlights including:
   - Editor of the month
   - Important milestones
   - Distillery Tips & Tricks
   - Educational resources
5. **Feedback & Support** - Contact information for user input

### Style Guidelines

All feature release communications must follow Distyl's brand voice:

- **Length**: ~150 words maximum when possible
- **Tone**: Professional yet casual, emotionally responsive
- **Brand Traits**: Human, casual, optimistic, accessible, energetic, approachable, "disruptively positive"
- **Perspective**: Always speak as "we/our" on behalf of Distyl (never third person)
- **Focus**: How features benefit customer experience and real use cases
- **Data-driven**: Base updates strictly on provided data, never speculate

### Reference Files

- `feature-release-specifications.md` - Complete template specification
- `feature-release-style-guide.md` - Brand voice, tone, and writing style guidelines
- Sources:
  - [Specifications](https://www.notion.so/2732c038ca378098baedd85657893e26)
  - [Style Guide](https://www.notion.so/2732c038ca3780a992f7eea7263cc65b)

### Data Source: Tracking Database

The automated feature update generator pulls data from the "Tracking Database" (Notion database within the Distillery: Improvement Tracker page).

**Database Details:**
- **Database ID**: `2702c038ca37805fb43cf18f5dde108d`
- **Data Source URL**: `collection://2772c038-ca37-802e-b11a-000bd46e0a43`
- **Location**: Embedded in [Distillery: Improvement Tracker](https://www.notion.so/2702c038ca3780628bccd98cd4dc5a26)

**Column Mapping:**
- **Title** = "What" (description of what the update accomplishes)
- **Column 1** = "Category" (determines document section placement)
  - `Feature: UX` → "Feature Updates" section
  - `Feature: Code` → "Behind the Scenes" section
- **Column 2** = "When" (implementation date)
- **Column 3** = "Why" (explanation of why users should care)
- **Column 5** = "Share Status" (tracking if included in previous releases)
- **Column 6** = "Release Version" (which version included this feature)
- **Files & media** = Screenshots/media files for features

**Status**: ✅ Database accessible with full read/write permissions for automated updates

**Section Mapping:**
- **Feature Updates**: Include items with Category = "Feature: UX"
- **Behind the Scenes**: Include items with Category = "Feature: Code"
- **Growth Spotlight**: Skip this section until Growth Spotlight data source is provided

**Automation Pipeline:**
1. Query Tracking Database for items with empty "Share Status"
2. Group by Category for proper section placement
3. Extract original filenames from Notion "Files & media" column URLs
4. Match filenames to local screenshot files in /Users/jcastillo/Desktop/snapshot folder
5. Embed real images from local snapshot folder using doc.add_picture() with proper sizing
6. Use "What" for feature description and "Why" for impact/value
7. Auto-generate 1-Minute Summary from feature data highlights
8. Create step-by-step "How it works" instructions for each feature (3 steps per feature)
9. Follow template structure and style guidelines
10. Generate Word document (.docx) output with embedded real screenshots
11. Mark ALL included items as "Shared" and update Release Version after publication (both Feature: UX and Feature: Code items)

**Configuration Settings:**
- **Output Format**: Word document (.docx)
- **Title Format**: "Routine Editor Newsletter" (no version numbers in title)
- **Date Display**: Centered current date below title (dynamically generated when program runs) - MUST be properly bold formatted, NOT markdown
- **Version Numbering**: Check Column 6 for highest existing version, increment by 0.01. If no versions exist, start at 1.01
- **Feedback Contact**: Juan@distyl.ai
- **Item Selection**: Include ALL unshared items unless explicitly instructed otherwise
- **Post-Publication Updates**: Update ALL featured items (both UX and Code categories) with "Shared" status and current release version
- **Summary Generation**: Auto-generate 1-Minute Summary from most impactful features

**Formatting Requirements:**
- **Emojis**: One professional emoji per feature (✅, 🚀, 📊, 🔒, etc.) before descriptions
- **Typography**: Bold headings, key outcomes, and text before colons
- **Whitespace**: Compact spacing - single paragraph breaks between features, minimal gaps
- **Visual Hierarchy**: Clear headings and subheadings for scannability
- **Numbering**: "How it works" steps use 1-3 numbering for EACH individual feature (not cumulative)
- **Screenshots**: MANDATORY - If available in "Files & media" column:
  - Extract original filenames from Notion file URLs using extract_image_filename()
  - Match filenames to local screenshot files in /Users/jcastillo/Desktop/snapshot folder using exact filename matching only
  - Embed real images using doc.add_picture(image_path, width=Inches(6))
  - ABSOLUTELY FORBIDDEN: placeholders, text references, mock images
  - REQUIRED: Only real embedded images from local snapshot folder are acceptable
  - All screenshots: 6 inches wide for consistent visual uniformity
  - Single or multiple screenshots all use same 6-inch sizing
  - Local snapshot folder approach eliminates authentication issues

### Reference Files

- `feature-release-specifications.md` - Complete template specification
- `feature-release-style-guide.md` - Brand voice, tone, and writing style guidelines
- Sources:
  - [Specifications](https://www.notion.so/2732c038ca378098baedd85657893e26)
  - [Style Guide](https://www.notion.so/2732c038ca3780a992f7eea7263cc65b)
  - [Improvement Tracker](https://www.notion.so/2702c038ca3780628bccd98cd4dc5a26)

### Usage Instructions

When creating new feature release documents:
1. Reference `feature-release-specifications.md` for structure and format
2. Follow `feature-release-style-guide.md` for tone, voice, and presentation
3. Query Improvement Tracker for unshared items using Category mapping
4. Maintain consistency with established brand voice and standardization