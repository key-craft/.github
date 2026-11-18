Keycraft

Crafting Code. Playing Music.

What if every line of code brought you one step closer to playing the piano?

Keycraft is an open-source initiative that transforms an 88-key digital piano into a complete computer keyboard, allowing software developers to write code, navigate applications, and operate their computers using piano keys instead of a conventional QWERTY keyboard.

Our ambition is simple:

Learn to play the piano while doing the work you already do every day.

⸻

🎹 One Keyboard. Two Disciplines.

Software engineering and piano playing have something remarkable in common.

Both require translating ideas into precise sequences of finger movements across a keyboard.

Yet we traditionally practice them separately.

Developers spend hours typing code on QWERTY keyboards, while aspiring pianists must find additional time to practice on musical keyboards.

Keycraft brings these two worlds together.

Instead of adding piano practice to an already busy schedule, we explore how daily computer interaction can contribute to developing musical skills.

The piano becomes both:

* A computer input device — for writing software, using applications, and navigating an operating system.
* A musical instrument — for developing finger coordination, learning scales, practicing chords, and ultimately playing music.

Keycraft does not assume that typing automatically teaches piano playing. Instead, it combines a new input method with deliberate musical exercises and measurable learning.

⸻

💡 The Idea

Imagine sitting behind an 88-key digital piano, connected to your laptop.

You open Visual Studio Code.

You write TypeScript.

You navigate your project.

You execute terminal commands.

You commit changes to Git.

And you do it all using the piano keyboard.

No conventional QWERTY keyboard is required for normal operation.

The same instrument can switch into Piano Mode, allowing you to practice music without changing your physical workspace.

The instrument you use to create software is also the instrument you are learning to play.

⸻

🏗️ How Keycraft Works

Keycraft translates musical keyboard input into computer keyboard events.

flowchart TD
    A["88-Key Digital Piano"]
    B["USB MIDI"]
    C["Keycraft Input Engine"]
    D["Keyboard Layout & Mapping"]
    E["Computer Keyboard Events"]
    F["Operating System"]
    G["IDE / Terminal / Browser"]
    H["Piano Learning Engine"]
    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G
    C --> H

The input engine interprets MIDI notes, note releases, pedal events, and combinations of keys.

A configurable mapping translates these musical gestures into ordinary computer input.

The resulting keyboard events are delivered to the operating system, allowing Keycraft to work with existing applications.

No special programming language or modified IDE is required.

Two Implementation Paths

Software-based Keycraft

A local application receives MIDI events and generates operating-system keyboard events.

This approach enables rapid experimentation with layouts, input strategies, and learning features.

Hardware-based Keycraft

A dedicated MIDI-to-USB-HID adapter translates piano input into standard keyboard events.

The computer recognizes the adapter as a conventional USB keyboard, reducing the need for specialized software on the host computer.

Both implementations share the same conceptual mapping and input behavior.

⸻

🎼 The 88-Key Keyboard

A full-size piano provides:

* 52 white keys.
* 36 black keys.
* 88 individually addressable note positions.
* Velocity-sensitive input on supported instruments.
* Optional pedals for additional control.

Keycraft organizes these inputs into configurable functional regions.

Region	Responsibility
System	Modifiers, operating modes, system commands
Left-hand typing	Letters and frequently used actions
Right-hand typing	Letters, punctuation, editing
Extended symbols	Numbers and programming symbols
Navigation	Cursor movement, selection, application navigation
Pedals	Layer switching, commands, musical sustain

Unlike QWERTY, Keycraft does not need to preserve a layout originally designed for mechanical typewriters.

We can explore layouts based on:

* Human hand anatomy.
* Piano fingering.
* Character frequency.
* Programming language syntax.
* Finger travel distance.
* Hand alternation.
* Musical intervals.
* Ergonomic comfort.

The goal is not simply to make piano keys behave like computer keys.

The goal is to discover a better relationship between human hands, musical instruments, and software creation.

⸻

🦶 Pedals as Input Controls

A digital piano equipped with three independently detectable MIDI pedals can provide additional interaction capabilities.

Pedal	Proposed role
Left	Symbol and character layers
Middle	Commands and application shortcuts
Right	Piano Mode switching and musical sustain

For example, holding the symbol pedal could change the output of selected keys from letters into programming punctuation.

The command pedal could expose frequently used IDE operations such as formatting code, navigating definitions, or opening a terminal.

Pedal behavior is configurable and depends on the capabilities of the connected instrument.

⸻

🎓 Learning Through Everyday Work

Keycraft is not only an alternative computer keyboard.

It is also an experiment in embedded learning.

The idea is to create opportunities for musical development within an activity that already occupies a significant part of a developer’s day.

The learning system may eventually support:

* Finger independence exercises.
* Hand coordination.
* Musical scales and intervals.
* Chord recognition.
* Rhythm and timing.
* Velocity and dynamic control.
* Musical notation.
* Personalized practice suggestions.
* Progress measurement.

A developer might spend 45 minutes programming and then complete a short musical exercise based on movements practiced during that session.

Over time, Keycraft aims to investigate whether these interactions can contribute to measurable piano-playing progress.

Actual musical learning remains a deliberate activity, supported rather than replaced by the programming interface.

⸻

🧩 Architecture

Keycraft is designed around reusable components and clear interfaces.

flowchart TD
    P["Keycraft"]
    P --> I["Input"]
    P --> M["Mapping"]
    P --> O["Output"]
    P --> L["Learning"]
    I --> I1["MIDI Events"]
    I --> I2["Pedals"]
    I --> I3["Key State"]
    M --> M1["Keyboard Layouts"]
    M --> M2["Input Layers"]
    M --> M3["Commands"]
    O --> O1["macOS"]
    O --> O2["Linux / Windows"]
    O --> O3["USB HID"]
    L --> L1["Exercises"]
    L --> L2["Feedback"]
    L --> L3["Progress"]

The architecture separates:

1. Input — receiving and normalizing piano events.
2. Mapping — interpreting those events as typing gestures.
3. Output — delivering keyboard actions to the host computer.
4. Learning — turning piano interaction into opportunities for musical development.

The core mapping engine should remain independent of any particular operating system or piano manufacturer.

This enables alternative layouts, different hardware implementations, and future extensions without rewriting the entire system.

⸻

🗂️ Proposed Repositories

Keycraft will grow through independently maintained repositories.

Repository	Purpose
keycraft	Main project and reference implementation
keycraft-core	MIDI interpretation and keyboard mapping engine
keycraft-layouts	Versioned 88-key keyboard layouts
keycraft-desktop	Desktop application and configuration
keycraft-hardware	MIDI-to-USB-HID hardware adapter
keycraft-learning	Piano exercises and learning feedback
keycraft-documentation	Architecture, specifications, and guides

These repositories represent the proposed organization structure. They will be introduced as the project evolves.

⸻

🚀 Roadmap

Phase 1 — The First Keystroke

Make a piano key type a character on a computer.

* Connect an 88-key MIDI piano.
* Receive MIDI note events.
* Translate notes into keyboard events.
* Support key press and release.
* Demonstrate text entry.

Phase 2 — The Programming Keyboard

Write software without using QWERTY.

* Implement a complete typing layout.
* Support programming symbols.
* Support modifiers and shortcuts.
* Integrate pedal-based layers.
* Support code editors, terminals, and browsers.
* Handle disconnections and stuck-key recovery.

Phase 3 — The Ergonomic Instrument

Make programming comfortable and efficient.

* Analyze typing frequency.
* Measure finger travel.
* Compare alternative layouts.
* Evaluate typing accuracy and speed.
* Improve hand balance.
* Test long-duration usability.

Phase 4 — The Learning Instrument

Connect programming practice to piano education.

* Introduce Piano Mode.
* Provide guided exercises.
* Track timing and coordination.
* Offer personalized practice.
* Measure musical learning progress.

Phase 5 — The Independent Keyboard

Make Keycraft usable as a standalone input device.

* Develop a hardware MIDI-to-HID adapter.
* Support standard USB keyboard input.
* Provide portable keyboard configurations.
* Reduce host software dependencies.
* Expand compatibility across operating systems.

⸻

🔬 Research Questions

Keycraft is also an exploration of human–computer interaction.

Some of the questions we want to investigate include:

Can a piano keyboard become a practical replacement for QWERTY?

Can we achieve sufficient typing speed, accuracy, and comfort for professional software development?

What does an ergonomic piano-based typing layout look like?

Should mappings prioritize character frequency, musical fingering, hand alternation, or a combination of these?

Can programming contribute to musical development?

Does regular interaction with a piano keyboard improve coordination, finger independence, or other measurable musical skills?

Can musical gestures become a new vocabulary for computing?

Could chords, intervals, dynamics, and pedals eventually enable forms of computer interaction that conventional keyboards cannot easily express?

These are open questions, not predetermined conclusions.

Keycraft intends to answer them through prototypes, experimentation, and evidence.

⸻

🔐 Privacy and Reliability

A keyboard is a sensitive input device.

Keycraft must be designed with security, reliability, and user control in mind.

Our principles include:

* Process input locally by default.
* Never require cloud services for ordinary typing.
* Avoid storing typed source code, passwords, or sensitive text.
* Collect learning metrics only with explicit user control.
* Recover safely from disconnected MIDI devices.
* Prevent stuck modifier keys and unintended shortcuts.
* Provide clear feedback about active input modes.
* Maintain an accessible fallback input method.

The computer must remain controllable even when Keycraft is unavailable.

⸻

🤝 Open Source and Collaboration

Keycraft is intended to be an open-source exploration.

We welcome contributions from:

* Software engineers.
* Pianists and music educators.
* MIDI and audio developers.
* Embedded systems engineers.
* Human–computer interaction researchers.
* Ergonomics specialists.
* Accessibility researchers.
* Curious makers and experimentalists.

There is room for many different approaches.

Alternative keyboard layouts, hardware adapters, learning techniques, and interaction models are all worth exploring.

The best design should emerge through experimentation and collaboration.

Contribution guidelines, licensing, and development processes will be published as the repositories mature.

⸻

🌍 Our Vision

For decades, the computer keyboard has primarily been treated as a tool for entering text.

The piano keyboard has primarily been treated as a tool for creating music.

Both are interfaces between human intention and physical expression.

What happens when we stop treating them as separate worlds?

Keycraft imagines a future where the tools we use for work can also help us develop new abilities.

Where writing software and learning music are not competing demands on our time.

Where everyday interaction becomes an opportunity to practice, explore, and create.

And where the keyboard is not merely something we type on.

It is something we learn to play.

⸻

Keycraft

Crafting Code. Playing Music.

Your next line of code is a step toward your next piece of music.

GitHub Organization
