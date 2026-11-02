# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

An Obsidian vault (synced via iCloud) holding university course materials for the 2026-2 semester. It is **not** a software project: there is no build, lint, or test setup, and no git repository. Most content is lecture PDFs; there are a few Markdown notes, Python/Jupyter lab files, and CSV datasets.

Content is primarily in Korean. Match the language of the surrounding material when writing notes.

## Layout conventions

- Top level: one folder per course, named `<N>.<과목명>(<분반>)`, e.g. `1.컴퓨터구조(02)`, `5.인공지능기초(01)`. The number is a display ordering, the parenthesized number is the class section.
- Inside each course: `week_1`, `week_2`, … folders holding that week's materials. Lab/practice material sits in a subfolder (e.g. `week_2/실습/`, `week_3/3주차-CAf-조합논리(가산기)실습/`).
- Course-wide references (textbooks) live directly in the course folder, not in a week folder.
- Notes are Markdown files placed alongside the source material for that week (e.g. `4.오픈소스하드웨어응용(01)/week_2/Arduino.md`).
- Ignore `.DS_Store` files and the `.obsidian/` config directory (one level up, in the vault root).

## Courses

| Folder | Course | Notes |
|---|---|---|
| `1.컴퓨터구조(02)` | Computer Architecture | Mano textbook PDF at course root; LogicWorks labs with 74-series datasheets |
| `2.자료구조(03)` | Data Structures | Python-based |
| `3.블록체인(01)` | Blockchain | |
| `4.오픈소스하드웨어응용(01)` | Open-Source Hardware Applications | Arduino / Tinkercad |
| `5.인공지능기초(01)` | Intro to AI | Lab code in `week_N/실습/` |
| `6.EE2(01)` | Essential English 2 | docx/pptx materials |

## Running lab code

The only executable code is in `5.인공지능기초(01)/week_*/실습/`: `.py` scripts and `.ipynb` notebooks using `pandas` and `scikit-learn`. They read CSVs by relative path, so run them from inside the `실습` directory:

```bash
cd "5.인공지능기초(01)/week_2/실습" && python "20235166 박서준.py"
```

Student ID `20235166` appears in submission filenames; keep that naming pattern for new lab submissions.
