# Lean Practitioner's Toolbox — Beta Tester Guide

Thanks for trying out **Lean Practitioner's Toolbox**! This is a short guide
to get you from "just downloaded it" to building your first artifact. It
covers the basics — enough to explore the app and give useful feedback.

Current version: **v2.0.1 (beta)** · macOS on Apple Silicon only (Windows
build planned, not yet available).

---

## What this app does

Lean Practitioner's Toolbox lets you build common Lean/Six Sigma process
artifacts without any flowcharting or drawing skills. You type structured
information into a sidebar on the left, and the app draws the diagram for
you on a canvas on the right — live, as you type.

Four artifact types are supported today:

- **SIPOC** — a high-level process map
- **Fishbone (Ishikawa)** — a root-cause / cause-and-effect diagram
- **X-Y Matrix** — a prioritization matrix
- **Value Stream Map (VSM)** — a process-flow map with timing

You don't need to be a Six Sigma practitioner to test the app — if you've
never used these tools before, the short explanation under each one below
should be enough to follow along.

---

## Installing

1. Download the DMG from the [releases page](https://github.com/The-Lean-Practitioner/lean-practitioners-toolbox-releases).
2. Open the DMG and drag **Lean Practitioner's Toolbox** into your
   Applications folder.
3. Launch it from Applications. The app is signed and notarized by Apple,
   so it should just open normally — no need to right-click → Open or
   adjust any security settings.

---

## The basics: Projects, Artifacts, and Tabs

Two words you'll see throughout the app:

- **Project** — the file you save (`.lean`). You have one project open at
  a time, much like a document.
- **Artifact** — one diagram inside a project (a SIPOC, a Fishbone, etc.),
  shown as a tab across the top. A single project can hold several
  artifacts — for example, a Fishbone for root-cause analysis and a VSM
  for the same process, side by side as tabs.

**Toolbar (top of the window):**

| Button | What it does |
|---|---|
| New | Start a fresh, empty project |
| Open | Open an existing `.lean` file |
| Save / Save As | Save your project |
| Close | Close the current project |
| Undo / Redo | Step backward/forward — acts on whichever artifact tab you're currently viewing |
| ⚙ Settings | Theme, font, and color preferences |

**Adding an artifact:** click the **+** button in the tab bar, pick a type
(SIPOC, Fishbone, XYM, or VSM), and give it a name. It appears as a new
tab.

Each tab has its own independent undo/redo history, and its own data —
editing one artifact never affects another.

---

## How editing works

The general pattern is the same across all four artifacts: **the sidebar
is where you type, the canvas is what you look at.** Click into a field,
type, and the diagram updates immediately. A few artifacts also let you
interact with the canvas directly (noted below) — but the sidebar is
always the source of truth.

Click **Save** often — there's no autosave.

---

## SIPOC

*A SIPOC maps a process at a high level across five categories:*
***S**uppliers, **I**nputs, **P**rocess, **O**utputs, **C**ustomers.* Use
it to scope out a process before diving into detail.

**In the app:** each of the five columns has its own **+ Add** button in
the sidebar. Click an item to edit it inline; press **Enter** to add the
next item in that column, or **Tab** to jump to the next column. The table
on the canvas builds itself to fit your content.

You can drag the vertical dividers between columns on the canvas to
resize them.

---

## Fishbone (Ishikawa)

*A Fishbone diagram helps a team brainstorm and organize potential causes
of a problem, grouped into major categories ("causes"), each with more
specific "sub-causes."*

**In the app:**

1. Click the diagram head (or the tree item at the top of the sidebar) to
   set your **Problem Statement**, owner, and date opened.
2. Click **+ Cause** to add a major cause — it appears as a "fin" on the
   diagram.
3. Select a cause to add up to 6 **sub-causes**, and to set its owner,
   due date, status, and priority.
4. Click any fin or sub-cause on the canvas (or in the sidebar tree) to
   jump straight to editing it.

Status colors (not started / in progress / blocked / complete) and
priority badges (P1–P5) show directly on the diagram.

---

## X-Y Matrix

*An X-Y Matrix helps prioritize which process inputs ("X's") most affect
the outputs your customers care about ("Y's"), by scoring the strength of
each relationship.*

**In the app:**

1. Add your customer-critical **outputs** in the sidebar, and rate each
   one's **importance** (1–10).
2. Add your process **inputs**.
3. On the canvas, click into any cell in the grid and score the
   relationship between that input and output (0–10) — directly on the
   canvas, not the sidebar, since a scoring grid works better as a grid.
4. Each input's **Total** (score × importance, summed across outputs) is
   calculated automatically. Use the sort button above the canvas to rank
   inputs high → low.

---

## Value Stream Map (VSM)

*A VSM lays out the steps in a process in order, distinguishing
value-added work (VA) from non-value-added work (NVA), so you can see
where time is actually going.*

**In the app:**

1. Click **+ Add Value-Added Step** or **+ Add Non-Value-Added Step** in
   the sidebar to add a step.
2. Click a step to expand it and fill in its title, owner (VA) or
   mitigation (NVA), description, and time.
3. Enter time as `15m` or `1.5h` — the app parses either format.
4. Use the ↑ / ↓ buttons to reorder steps.

The bottom of the canvas shows a running **VA Time**, **Total Time**, and
**Efficiency %** (VA time ÷ total time) — recalculated automatically as
you edit.

---

## Settings

Click the **⚙ Settings** button in the toolbar to adjust:

- Light/dark theme
- Font family and size
- Canvas background color
- Status colors (used on Fishbone causes)

---

## Exporting

Every artifact has an **Export SVG** button above the canvas. This saves
a standalone SVG file of just that diagram — handy for dropping into a
report, slide deck, or email.

---

## What's not in this beta

This is an early beta — a few things you'll notice are missing:

- No in-app help — this document is it, for now
- Windows isn't available yet (macOS Apple Silicon only)
- No fifth artifact type (an A3 report format is being considered)

---

## Reporting bugs & feedback

Found something broken, confusing, or worth suggesting? Please open an
issue on the releases repo:

**[github.com/The-Lean-Practitioner/lean-practitioners-toolbox-releases/issues](https://github.com/The-Lean-Practitioner/lean-practitioners-toolbox-releases/issues)**

A short description, what you expected vs. what happened, and (if
relevant) which artifact type you were using is all really helpful.
Comments or DMs on the LinkedIn post work too, if that's easier.

Thanks again for testing — it genuinely helps.
