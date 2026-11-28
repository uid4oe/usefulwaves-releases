# usefulwaves

Dictate into Mac apps with on-device speech recognition. Rewrite selected text and attach screenshots as you speak.
Record meetings and QA reviews, then hand the work to Codex or Claude Code.

[Explore usefulwaves for Mac](https://usefulwaves.web.app/) or [download the latest release](https://github.com/uid4oe/usefulwaves-releases/releases/latest).
The tour shows dictation, Quick Actions, screen capture, meetings, QA reviews, and saved captures with screenshots from the Mac app.

## Requirements and installation

The distributed app requires Apple Silicon and macOS 15 or later.
Apple Intelligence also requires macOS 26 and supported hardware.

1. Download the DMG from Releases. Quit any running copy before installing.
2. Open the DMG and drag `usefulwaves.app` into Applications.
3. Open the app and complete setup.
4. Allow microphone and Accessibility access when macOS requests them.
5. Choose a speech engine and your shortcut.

These releases are not notarized by Apple.
If macOS blocks the first launch, use System Settings → Privacy & Security → Open Anyway.
Sparkle checks for signed updates after installation.

## Dictation

Press the shortcut to start recording. Focus the destination input and press the shortcut again to stop.
Keep that input focused while usefulwaves transcribes your speech on the device.
If usefulwaves cannot verify the destination, choose **Copy Text** and paste the transcript yourself.
To polish dictation before pasting, turn on **Enable AI features** and **Use AI processing for dictation** in Settings → AI processing.
Hold the stop shortcut until the green outline appears to request Return after pasting.
In a terminal that exposes only its window, usefulwaves pastes plain text into the window focused at stop.
Typing or clicking in that window during transcription cancels the paste.
Even a held stop leaves that draft for you to submit. The overlay shows **Return skipped**.

## Quick Actions

Select text and press the shortcut to open writing tools when AI is available.
Choose an action, speak a custom instruction, or type one.
Results appear in the card as generation progresses when the connection supports streaming.
Choose **Apply** to replace the original selection if it is still editable and unchanged.
Choose **Copy** to copy the completed draft, including for terminal output, other read-only text, or a changed selection.
Customize the actions in Settings.

## Screenshots

Choose **Capture Screen** during dictation and drag over a region. Repeat for each screenshot.
Focus the destination input before stopping. Rich text editors that support attachments receive the transcript and screenshots together.
In the Slack, Codex, and Claude desktop apps, usefulwaves pastes the transcript first, then each screenshot in capture order.
In Herdr, each screenshot follows the transcript as a separate PNG file. The draft stays open for review.
If delivery stops between attachments, use the numbered copy actions to paste the remaining screenshots one at a time.
To save the transcript and screenshots together as one local note, enable **Save screenshot dictations as captures** in Settings → Dictation.
Text-only dictation still pastes.
Use **Capture Screen Region** from the menu bar to type beside a preview.
Save the preview and your request as a capture. Enable local text recognition for the screenshot when needed.

## Speech engines

| Engine | Purpose |
|---|---|
| Parakeet Ultra | Default on Apple Silicon; multilingual recognition |
| Parakeet Redux | Smaller Parakeet alternative |
| Apple Speech | Built-in on-device recognition |

Downloadable engines require model files during setup.
Recording and transcription run on the device.

## AI processing

Use installed Claude Code or Codex CLIs with their existing subscription login.
Install and sign in through the command first, then add its connection in usefulwaves.
CLI connections send text to their provider servers. Account limits still apply.
usefulwaves does not store CLI login credentials.

API-key connections include OpenAI, Anthropic, Google Gemini, xAI, OpenRouter, and custom OpenAI-compatible endpoints.
Cloud providers can require your own credentials and charge for use.
Ollama and available Apple Intelligence offer local processing options.
Settings separates provider connections, model selection, reasoning options, and processing behavior.

Vocabulary entries preserve names and technical terms during AI processing.
Cloud AI receives those entries with the text submitted for processing.

## Meetings

Record your microphone or your microphone with system audio.
Meetings use the input device selected in Dictation.
System capture includes application audio and requests macOS permission when needed.
Pause and resume recording, then transcribe saved audio with your local speech engine.
Completed audio parts and transcription progress remain available after interruption.

Correct transcript passages, then prepare cited notes and work briefs through your chosen AI connection.
Recording and transcription work without AI processing.
Review statements and source evidence before copying a brief or exporting the meeting.
Export the meeting to Markdown. Audio stays on your Mac.
Take prepared work to the human or agent workflow you prefer.

## QA Reviews

Start a QA review to record a walkthrough on your Mac.
Add screen regions from the floating panel. Use the menu bar to add selected text.
Choose **Next Finding** when you move to another topic.
Open the saved review to inspect each finding and its evidence or read the transcript.

## Captures and workflows

Save a note, checklist, screenshot, selection, or Quick Action result as a capture.
Edit the capture in Markdown and keep its source evidence beside the task.
Copy the task or export Markdown when you want to share it.

Open a note or to-do in Codex to review before sending. usefulwaves copies the task when opening Claude.
With Herdr Core, run a configured workflow and open its live terminal below the capture.
Use **Restore Default Workflows** in Settings to restore missing profiles for detected Codex and Claude Code CLIs.
Enable local MCP access in Settings to let a configured assistant read saved captures.

## Privacy and local data

Audio capture runs during recording. Speech recognition runs locally.
Optional cloud AI receives submitted text and the applicable instructions through API or CLI connections.
History stores transcription records locally. Manage them in the History tab.
usefulwaves stores meeting audio, transcripts, and prepared work on your Mac. Exporting a meeting leaves its local record in place.
Provider credentials stay in an owner-only file on the Mac.
Diagnostics include local timing and error logs.
Captures, attached source evidence, and personalization are stored on your Mac.

## Distribution

usefulwaves is closed source.
The first public release is 0.0.1.
This repository hosts release information and the Sparkle update feed.
Release assets contain the compiled app and required runtime resources.
The private application source, development files, and signing keys are not distributed.
