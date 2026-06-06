# Velum: The Complete Voiceover Ecosystem

After months of coding, compiling, and entirely too much tea, I'm incredibly proud to release the Alpha of Velum. 

Velum is the world's first end-to-end workflow ecosystem and specialized Digital Audio Workstation designed specifically for professional Voice Over production, ADR, and remote collaboration. By bypassing the bloat of traditional music-focused DAWs, it offers a streamlined, VO-first feature set.

<img width="1904" height="1048" alt="Main_App_Window" src="https://github.com/user-attachments/assets/a267e93c-faba-4d55-b03b-aa8ff2678f91" />

Here is what you can expect in our first major release:

### Distraction-Free, High-Performance Audio
* Velum is powered by a high-performance Rust backend that provides direct, uncolored access to your input devices.
* It achieves zero-latency monitoring and operates natively in 32-bit Float, ensuring practically infinite dynamic headroom internally.
* To prevent UI freezing, the canvas utilizes PixiJS to batch and draw waveforms incrementally at 60fps on the GPU.

<img width="1904" height="1048" alt="Audio_Configuration" src="https://github.com/user-attachments/assets/1dcdccf6-24a6-460f-be0a-16297c733142" />

### The Actor's Toolkit
* The built-in Script Reader automatically parses and formats Fountain syntax right next to your waveform.
* Use the manual "POP OUT" feature to open your script in a completely separate window. You can then switch to "Prompt Mode" to focus entirely on your read without the distractions of the DAW in your peripheral vision.
* Visually track your read speed against strict time limits using the Pacing Bar.
* Essential ADR tools are included, allowing you to load a video file into the built-in player to record audio in time with the picture.

### True End-to-End Casting & Submission
* When browsing open roles on the Velum website, clicking "Open in Desktop App" triggers a secure deep link that instantly configures the DAW to the Casting Director's exact specifications, including sample rate and bit depth.
* The required script snippet is automatically injected directly into your Script Reader.
* **Zero-Friction Submissions:** When you finish recording, simply click the "Submit Audition" button. Velum automatically routes your high-res audio directly to the dashboard inbox of the director who created the casting call. No manual file naming, exporting, or emailing required.

### Manual Exports & ACX Checking
* **In-App Audio Checker:** Instantly verify your audio output against strict ACX standards using the built-in checker without needing to leave the app.
* **Background Processing:** When manually exporting files, you can run your audio editing and processing tasks in the background, allowing you to keep working while Velum handles the heavy lifting.

### Live Remote Direction & "Auto-Replace"
* The native Connect Panel is powered by a hybrid WebRTC/Supabase engine, allowing casting directors to listen to your raw microphone feed in real-time directly from their browser.
* When you stop recording, Velum's "Auto-Replace" automatically swaps the compressed stream proxy on the director's end with your pristine, uncompressed 32-bit local `.wav` file.

<img width="1904" height="1048" alt="Remote_Connection" src="https://github.com/user-attachments/assets/3355d918-e1fc-4242-b602-20ff3e75fa75" />

### Zero-Loss Crash Recovery
* Never lose a take to a power outage again.
* Velum writes raw `f32` PCM data directly to disk as you record, bypassing standard `.wav` header finalization that corrupts during crashes.
* On your next startup, the Crash Recovery Modal detects abandoned chunks and auto-restores the clips to their exact temporal positions on the timeline.

### Known Limitations & Alpha Notes
* Velum requires an active internet connection to log in and sync with the Casting Board.
* However, all audio recording, DSP processing, and saving operates entirely offline on your local machine.
* Because Velum is currently in Alpha, you may encounter bugs or crashes.
* If you do, please use the Bug Report Modal to securely send your anonymous system logs and audio hardware setup directly to me. There is no "engineering team." It is just me, alone, in a shed in the UK. Drinking tea and desperately trying to patch issues before my biscuit gets too soggy to dunk.
