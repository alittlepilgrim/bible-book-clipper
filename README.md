# Bible Chapter Clipper Automation (Mac)

This AppleScript automates the process of navigating through Bible chapters on the [USCCB Bible website](https://bible.usccb.org), allowing you to manually clip each chapter into Obsidian using the Web Clipper. It flips through pages, refocuses the browser, clicks to ensure keyboard shortcuts work, and plays a voice prompt so you know when it’s time to clip.

##  What It Does

- Opens Safari to the first chapter of the selected book
- Navigates through all chapters sequentially
- Refocuses Safari and clicks the page to ensure keyboard input
- Plays a custom voice cue (e.g., you saying "Next") when the page is ready
- The voice cue (or a manual trigger) will activate the Obsidian Web Clipper shortcut

---

##  Requirements

- macOS
- [cliclick](https://github.com/BlueM/cliclick) installed via Homebrew:
  ```bash
  brew install cliclick

	•	Safari browser
	•	Obsidian with the Web Clipper extension installed
	•	A recorded .m4a or .aiff file of your voice saying “Next”

⸻

 Setup Instructions

1. Save Your Voice Prompt

Record yourself saying “Next” using the Voice Memos app:
	•	Open Voice Memos → Record: “Next”
	•	Tap “Share” → Save to Files → Choose Desktop
	•	Rename the file to: next.m4a

2. Save the Script

Paste the full AppleScript into Script Editor or save as bible-script.txt.

Update the values in this section:

set startChapter to 1
set chapterCount to 24
set bookName to "joshua"

3. Run the Script

You can run the script via Script Editor or save it as an application for easier reuse.

⸻

 How to Use
	1.	Launch the script.
	2.	It will open the first chapter in Safari.
	3.	Wait until you hear your recorded “Next” cue.
	4.	This voice command (e.g., “Next”) will trigger Shift + Option + O using macOS Voice Control or another tool which will trigger the Obsidian Webclipper.
	5.	Repeat for each chapter.

⸻

Setting Up a Voice Command on macOS (Optional)

To automate triggering Shift + Option + O:
	1.	Open System Settings → Accessibility → Voice Control
	2.	Turn on Voice Control
	3.	Click Commands…
	4.	Click + to add a new command:
	•	When I say: "Next"
	•	While using: Safari
	•	Perform: Press keyboard shortcut
⇧ + ⌥ + O

Now whenever you say “Next”, it triggers the Web Clipper shortcut.

⸻
 Notes
	•	The script assumes Safari is the only browser involved.
	•	Adjust coordinates in the cliclick command if needed.
	•	You can customize the delay (delay 3) depending on how much time you need to clip.

⸻

Credits

Built for efficient, semi-automated Scripture clipping and organization in Obsidian. Compatible with USCCB’s web structure.
