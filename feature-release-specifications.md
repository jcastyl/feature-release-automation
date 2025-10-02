# Feature Release: Specifications

**Goal:** The purpose of this document is to outline a standardized structure for feature release updates in order to later automate the process by using AI

---

## Title Format
# Routine Editor Newsletter

**[Dynamic Current Date - Must be properly bold formatted in Word document, NOT markdown]**

---

## Formatting Guidelines

**Output Format:** Word document (.docx)

**Visual Structure:**
- **Headings & Subheadings:** Use bold or header styles for each feature to improve scannability
- **Whitespace:** Compact spacing - single paragraph breaks between features, avoid excessive gaps
- **Emojis:** Use 1 per feature description - simple, professional ones (✅, 🚀, 📊, 🔒, etc.)
  - Place emojis before feature descriptions, left-justified as visual anchors
- **Highlights:** Use bold to emphasize key outcomes/benefits and text before colons
- **Numbering:** Each feature's "How it works" uses 1-3 numbering (reset for each feature, not cumulative)
- **Screenshots:** MANDATORY - Include from "Files & media" column when available:
  - Extract original filenames from Notion file URLs using extract_image_filename()
  - Match filenames to local screenshot files in /Users/jcastillo/Desktop/snapshot folder using exact filename matching only
  - Embed real images from local snapshot folder using doc.add_picture()
  - ABSOLUTELY FORBIDDEN: placeholders, text references, mock content
  - REQUIRED: Only real embedded images from local snapshot folder are acceptable
  - All screenshots: Centered below feature header (6 inches wide)
  - Consistent 6-inch sizing across all screenshots for visual uniformity
  - Local snapshot folder approach eliminates authentication issues

---

## 1-Minute Summary
- [Insert 2–3 key highlights with their impact on users]

---

## Feature Updates

### [Feature Name]
- **What's new:** [Brief description of the update]
- **Impact:** [Explain why it matters / how it improves workflow]
- **How it works:**
	1. [Step 1 - user action to access/initiate feature]
	2. [Step 2 - system behavior or next user action]
	3. [Step 3 - result or completion action]

---

## Behind the Scenes

### Reliability Improvements
- **Impact:** [Benefit to users, e.g., fewer errors, faster processing]
- **Changes:**
	- [Change 1: infrastructure/db/etc.]
	- [Change 2: monitoring/metrics/etc.]

### System/Performance Updates
- **Impact:** [How these affect reliability, speed, or accuracy]

---

## Growth Spotlight
- Editor of the month (most accepted proposals)
- Highlight important milestones
- Distillery Tips & Tricks
	- The purpose is to encourage people to use underutilized features in the Distillery
- Highlight new educational resources

---

## Feedback & Support
We'd love your input!
- **Feedback:** [Feedback channel/email/contact]

**Best regards,**
*The Distyl Team*