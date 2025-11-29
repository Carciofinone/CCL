CCL (CyclomotoCycloramicLegacy) collects two related camera utilities and example code for automated multi‑shot capture tied to device rotation/heading. This repo includes the original Cycloramic 32‑bit files and a rebuilt 64‑bit version that runs on iPhone 5s. All usage instructions, configuration options, and build notes are provided below.
What’s included
• Original Cycloramic 32‑bit files (kept for historical/reference purposes).
• 64‑bit Cyclomotor/Cycloramic build (targeted to run on iPhone 5s).
• Example ViewController.swift demonstrating: numeric step capture, degrees‑per‑step, compass‑based triggers with fallback timed burst, flash/torch sync, optional triple end flash signal, and horizontal merge of captured images in reverse order.
• Settings UI to configure steps, degrees, tolerance, merge mode, start delay, and end‑flash toggle.
Features
• Configurable steps and degrees per step (positive or negative).
• Compass‑driven capture with heading tolerance and haptic feedback.
• Timed fallback when heading is unavailable.
• Flash handling: camera flash when available; torch simulation otherwise.
• Merge images horizontally in reverse order (last → first) or save individually.
• Optional triple torch flash at sequence end to signal completion (toggleable).
• Saves to Photos using UIImageWriteToSavedPhotosAlbum.
Compatibility and notes
• 64‑bit build included and tested on iPhone 5s.
• Original 32‑bit Cycloramic files are included for reference.
• Untested on iPhone 6 and 6s — I have not tried the 64‑bit build on those models. Results may vary; compass and torch behavior depend on device hardware and iOS version.
• Requires physical device for compass/torch features; simulator will not reproduce those behaviors.
• Make sure Info.plist contains NSCameraUsageDescription and NSLocationWhenInUseUsageDescription.
Build and install
1. Open the Xcode project or workspace in this repo.
2. Select a physical device (iPhone 5s or newer) as the run target.
3. Ensure required Info.plist keys are present.
4. Build and run. If you encounter permission prompts, allow camera and location access.
5. Use the Settings button in the app to configure steps, degrees, tolerance, merge mode, start delay, and end‑flash signal.
Troubleshooting
• If captures are missed, increase heading tolerance in settings.
• If merge fails due to memory, switch to save individually mode.
• If torch/flash behavior is inconsistent, test on another device or disable torch simulation.
License and contribution
• Add your preferred license file (e.g., MIT) to the repo.
• Contributions and pull requests are welcome. Please open issues for bugs or feature requests.
Contact
If you want the full Xcode project file or a packaged build, email me and I will provide the file on request.
