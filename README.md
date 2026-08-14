# Accessibility Tree

A free, open-source, cross-platform accessibility tool combining screen
magnification, screen reading, color filtering, cursor enhancement,
keyboard echo, and voice commands. Built on Java 21 LTS behind a common set
of interfaces, with platform-specific backends underneath.

## Goal overview

| Goal | Cross-platform? | OS Difficulty | Implementation Difficulty (based on my assumptions)
|---|---|---|---|
| Keyboard echo | Yes, out of the box | Low | Low |
| Voice commands | Yes, out of the box | Low–Medium | Hard |
| Text-to-speech | Yes (external process) | Low | Medium |
| Color filters | Yes (pure rendering) | Low | Medium |
| Cursor enhancement | Partial | Low–Medium | Low |
| Magnification | No - per-OS | Medium | Hard |
| Screen reading | No - per-OS | Medium–High | Hard |

> **Important:** Keyboard echo specifically poses a security risk as it is essentially a keylogger by construction.

---

## Goals

### 1. Keyboard Echo

**What it does:** speaks each key as it's pressed.

---

### 2. Voice Commands

**What it does:** a small fixed vocabulary - "zoom in," "read line,"
"stop"

---

### 3. Text-to-Speech

**What it does:** underlies keyboard echo, screen reading output, and
voice-command confirmations.

---

### 4. Color Filters

**What it does:** recolors text/background for contrast - e.g.
inverted, high-contrast, specific color-blind-friendly palettes.

---

### 5. Cursor Enhancement

**What it does:** enlarges and/or recolors the mouse cursor beyond OS
defaults.

---

### 6. Magnification

**What it does:** system-level zoom with keyboard/mouse/voice control,
beyond standard OS magnifier limits.

---

### 7. Screen Reading

**What it does:** reads on-screen text aloud by walking the OS
accessibility tree. It may become useful to include OCR but 
this is a stretch goal at best.