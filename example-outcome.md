# Curriculum: Custom Smartphone Ringtone Generator with Python & AI

Welcome to this 6-hour interactive workshop. Master **Large Language Models (LLMs)** and **Prompt Engineering** using the practical task of building a custom smartphone ringtone via Python as your learning vehicle. 70% of your time will be spent collaborating directly with AI to structure logic, debug, and design software specifications.

---

## Learning Outcomes

### Subject-Matter Outcomes (Python & Audio)
* Load, manipulate, and export audio files using Python audio libraries.
* Implement programmatic audio editing: trimming, volume adjustment, and fades.
* Format audio output for smartphone compatibility (MP3 for Android, M4R for iOS).

### AI Literacy & Prompt Engineering Outcomes
* **Zero-to-Hero Prompting:** Transition from simple queries to structured, system-persona-driven prompts.
* **Co-Pilot Workflow:** Treat LLMs as active collaborative engineering partners.
* **Code Verification:** Recognize LLM hallucinations and run structured debugging loops.
* **Specification Design:** Author technical specs that prompt an AI to generate production-ready code instantly.

---

## Assumed Knowledge
* Basic computer literacy. No prior Python experience required.

---

## Session 1 — Getting Started

* **Learning Objectives:** Understand LLM context windows; set up a basic Python environment via AI.
* **Key Concepts:** Token prediction, LLM context, audio library architecture.
* **Prompt Techniques:** Goal definition, establishing context.

### LLM Knowledge
LLMs calculate probabilities to predict the next logical word (token). Providing precise context narrows down these probabilities, drastically improving script accuracy.

### Practical Exercise Summary
Prompt the AI to guide you through installing Python, setting up a virtual environment, and installing necessary audio libraries. Verify the setup using an AI-generated verification check.

### Prompt Challenge & Example Prompts
> **The Challenge:** Prompt the AI to explain Python and audio library installation without using confusing developer jargon.

* **Weak Prompt:** *How do I use audio in Python?*
* **Effective Beginner Prompt:** "I am a complete beginner wanting to create a smartphone ringtone. Act as a patient Python tutor. Explain what libraries I need to process audio, and provide a step-by-step guide to installing them on my computer. Keep the language simple and free of overly technical jargon."

### Common Mistakes & Reflection
* **Mistake:** Running AI commands without asking what those steps actually do.
* **Reflection:** Why did adding "Act as a patient Python tutor" change the clarity of the AI's response compared to a generic search query?
* **Tip:** Always tell the AI your exact skill level so it scales its explanations appropriately.

---

## Session 2 — Asking Better Questions

* **Learning Objectives:** Isolate audio segments; apply constraints and personas to LLM interactions.
* **Key Concepts:** Millisecond-based audio slicing, system personas, negative constraints.
* **Prompt Techniques:** Persona adoption, explicit constraints, iterative follow-up.

### LLM Knowledge
Assigning a specific **Persona** (e.g., "Senior Audio Engineer") forces the LLM to pull from specific vectors in its training data, resulting in cleaner, more professional workflow structures.

### Practical Exercise Summary
Collaborate with the AI to map out the mathematical logic behind cutting exactly 30 seconds out of a track at a specific timestamp, adjusting decibel thresholds to boost volume for phone speakers.

### Prompt Challenge & Example Prompts
> **The Challenge:** Improve your previous prompt. Ask the AI to explain a slice script, but explicitly forbid it from using complex external dependencies or alternative libraries.

* **Improved Prompt:** "Act as a Senior Python Developer. Explain a clean strategy using only the core audio library to cut a 30-second clip from an MP3 file starting at the 1-minute mark. Do not suggest any other audio packages. Include a breakdown explaining how milliseconds are calculated."

### Common Mistakes & Reflection
* **Mistake:** Opening a new conversation window and losing all the setup context from Session 1.
* **Reflection:** How did setting a negative constraint ("Do not suggest any other audio packages") save you from downloading unnecessary software?
* **Tip:** If the AI gives an explanation that is too complex, ask it to: *"Simplify this specific section for a beginner."*

---

## Session 3 — Prompt Engineering

* **Learning Objectives:** Add audio fade effects; build reusable prompt templates with structural components.
* **Key Concepts:** Audio fade mechanics, Few-Shot prompting (providing examples).
* **Prompt Techniques:** Markdown delimiters, few-shot conditioning, reusable variables.

### LLM Knowledge
LLMs respond exceptionally well to clean layout structures like Markdown headers, bullet points, and parameter brackets. Providing structural examples (Few-Shot prompting) ensures highly predictable outputs.

### Practical Exercise Summary
Guide the AI to inject fade-in and fade-out effects into the audio logic so the ringtone doesn't start or stop abruptly. Extract the logic of your prompt into a text-based form template.

### Prompt Challenge & Example Prompts
> **The Challenge:** Create a reusable text template where you can easily swap out variables (like file names or timestamps) to generate new prompt modifications instantly.

* **Reusable Prompt Template:**
  System: You are an expert audio scripting assistant.
  Task: Add fade effects to an audio segment.
  Variables: FADE_IN: [INPUT_FADE_IN_MS]; FADE_OUT: [INPUT_FADE_OUT_MS]
  Instructions: Take the existing audio logic and apply a fade-in of FADE_IN and a fade-out of FADE_OUT. Provide only the updated steps.

### Common Mistakes & Reflection
* **Mistake:** Writing prompts as one massive paragraph, causing the AI to miss minor instructions.
* **Reflection:** How does using structured delimiters like `Variables:` change how reliably the AI follows your instructions?

---

## Session 4 — Specifications

* **Learning Objectives:** Export audio to custom bitrates/extensions; translate vague ideas into explicit functional specs.
* **Key Concepts:** Audio wrappers and codecs (MP3 vs M4R), bitrates, system paths.
* **Prompt Techniques:** Spec-driven prompting, setting strict output targets.

### LLM Knowledge
Providing an AI with a structured technical specification sheet eliminates ambiguity. The model stops guessing your intent, lowering the risk of generating broken logic.

### Practical Exercise Summary
Formulate a deployment specification sheet detailing how to export and save your finished audio clip into both high-quality MP3 (Android) and M4R (iOS) file formats, ensuring cross-platform compatibility.

### Prompt Challenge & Example Prompts
> **The Challenge:** Convert the vague request *"Make my ringtone save for an iPhone"* into a clear specification prompt for the AI.

* **Specification Prompt:**
  ### Objective: Export a processed audio segment into an iPhone-compatible ringtone format.
  ### Success Criteria: 1. Output file must have the extension `.m4r`. 2. Audio format must utilize the native container string. 3. Logic must specify a constant bitrate of 192k.
  ### Output Required: Provide the specific export configuration commands with brief explanations for each argument.

### Common Mistakes & Reflection
* **Mistake:** Assuming the AI knows your operating system, which changes how file paths and terminal exports are formatted.
* **Reflection:** Why did defining the success criteria beforehand prevent the AI from generating generic, unhelpful configurations?

---

## Session 5 — Working with AI

* **Learning Objectives:** Spot and fix AI hallucinations; isolate environment dependency bugs; implement safety loops.
* **Key Concepts:** System multimedia dependencies (FFmpeg), error parsing, fallback blocks.
* **Prompt Techniques:** Debugging loops, critical review prompting, error auditing.

### LLM Knowledge
LLMs often assume your environment is perfectly configured. If a system dependency like `FFmpeg` is missing, the AI might hallucinate programming fixes instead of telling you to install the underlying software. You must query the AI critically.

### Practical Exercise Summary
Intentionally introduce errors or paste typical environment warning logs into the AI. Practice managing a structural troubleshooting loop, directing the AI to isolate local file-path issues from system backend dependencies.

### Prompt Challenge & Example Prompts
> **The Challenge:** Feed an error message directly to the AI, but instruct it to analyze *why* the error happened before it proposes any changes.

* **Effective Debugging Prompt:** "I ran the script and received this error: `RuntimeError: Cannot find ffmpeg`. Act as an IT Systems Engineer. First, diagnose the root cause of this error. Second, provide instructions to fix it on my system. Do not rewrite my script logic yet."

### Common Mistakes & Reflection
* **Mistake:** Blindly pasting errors into the AI over and over without reading its explanations.
* **Reflection:** How does pausing to ask the AI for a *diagnosis* prevent it from making unnecessary changes to your working logic?

---

## Session 6 — Final Project

* **Learning Objectives:** Build a comprehensive, user-interactive application via structured AI collaboration.
* **Key Concepts:** User inputs, dynamic variables, automated file deployment workflows.
* **Prompt Techniques:** End-to-end specification enforcement, multi-turn review.

| Project Component | Requirements |
| :--- | :--- |
| **User Input** | Script prompts user for a local file path dynamically. |
| **Custom Slicing** | User defines start and end times via input variables. |
| **Polished FX** | Automated 2-second fades applied to both ends. |
| **Dual Export** | Outputs both `.mp3` and `.m4r` versions automatically. |

### Your Task
1. **Write your own specification sheet** utilizing the skills learned in Session 4.
2. **Design a prompting strategy** (Persona, constraints, templates).
3. **Execute the prompt** and collaborate with your AI partner to map, refine, and compile the final complete logic flow.

### Expected Final Output Architecture Summary
Your final workspace will feature a fully operational script structure that gracefully handles bad file inputs, interprets user timestamps in seconds, applies volume normalization along with dual fade transitions, and outputs fully optimized ringtone files ready for deployment to any iOS or Android device.

### Evaluation & Final Reflection
* How did your approach to prompting change from the quick questions in Session 1 to the detailed architecture specs you used in Session 6?
* How can you apply this collaborative engineering framework to other automation tasks in your professional career?