# LaTeX Template Maintenance Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Make the SDUT undergraduate LaTeX template easier to use from a fresh clone.

**Architecture:** Keep the template structure unchanged: `main.tex` remains the entrypoint, reusable content stays under `data/`, and formatting remains in `csbachelor.cls` / `csbachelor.cfg`. This maintenance pass only fills missing includes, documents the build path, and cleans generated files from version control.

**Tech Stack:** LaTeX, XeLaTeX-compatible template class, Git.

---

### Task 1: Complete Included Template Files

**Files:**
- Modify: `main.tex`
- Modify: `data/cover-en.tex`
- Create: `data/agreement.tex`
- Create: `data/bibliography.tex`
- Create: `data/acknowledgment.tex`

- [ ] **Step 1: Fix broken includes and title variable**

Update `main.tex` to include `data/abstract-en`, `data/chapter-5`, and `data/chapter-6`. Update `data/cover-en.tex` so the English title uses `\sduttitlee`.

- [ ] **Step 2: Add missing include files**

Add placeholder agreement, bibliography, and acknowledgment files so `main.tex` can compile without deleting required sections.

### Task 2: Improve Repository Usability

**Files:**
- Modify: `.gitignore`
- Modify: `README.MD`

- [ ] **Step 1: Expand ignore rules**

Ignore common LaTeX intermediate files, build directories, editor metadata, and OS metadata.

- [ ] **Step 2: Document quick start**

Add project structure and XeLaTeX build instructions for Chinese users cloning the template.

### Task 3: Verify And Commit

**Files:**
- Remove from index: `.DS_Store`
- Remove from index: `data/.DS_Store`
- Remove from index: `main.toc`
- Remove from index: `main.bbl`
- Remove from index: `main.blg`

- [ ] **Step 1: Remove generated or system files from git tracking**

Use `git rm --cached` so local copies remain available but future commits keep the repository clean.

- [ ] **Step 2: Build the template**

Run a XeLaTeX-compatible build command and confirm whether it succeeds. If the bundled Tectonic path cannot fetch packages in the sandbox, report the exact blocker.

- [ ] **Step 3: Commit and push**

Commit with a Chinese maintenance message and push `master` to the configured `origin` remote.
