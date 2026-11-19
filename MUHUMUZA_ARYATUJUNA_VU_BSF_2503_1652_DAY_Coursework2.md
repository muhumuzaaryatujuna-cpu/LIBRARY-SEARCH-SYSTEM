# BCS 2204 – Data Structures and Algorithms
## Group Coursework 2: Library Search Index

* **Student Name:** MUHUMUZA ARYATUJUNA
* **Registration Number:** VU-BSF-2503-1652-DAY
* **Programme:** BSF (Bachelor of Science in Software Engineering)
* **Session:** DAY
* **Group:** Group 1 (Library Search Index)
* **Assigned Component:** File Load and Save (Persistence & Sorted Export)
* **Submission Date:** 19 November 2026
* **GitHub Repository:** https://github.com/muhumuzaaryatujuna-cpu/LIBRARY-SEARCH-SYSTEM
* **Demo Video Link (CapCut):** `[PASTE_CAPCUT_VIDEO_LINK_HERE]`

---

## 1. System Overview & Group Allocation Table (11 Members)

| # | Member Name | Registration Number | Assigned Component | Status |
|---|---|---|---|---|
| 1 | MUHUMUZA ARYATUJUNA | VU-BSF-2503-1652-DAY | File Load and Save (pipe-delimited parsing, validation, A–Z save) | Completed |
| 2 | Pheiona Nakatte | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 3 | Bakasinga Gerald | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 4 | `[EDIT: Member 4 Name]` | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 5 | `[EDIT: Member 5 Name]` | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 6 | `[EDIT: Member 6 Name]` | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 7 | `[EDIT: Member 7 Name]` | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 8 | `[EDIT: Member 8 Name]` | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 9 | `[EDIT: Member 9 Name]` | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 10 | `[EDIT: Member 10 Name]` | Pending | `[EDIT: Assigned Module]` | Pending Edit |
| 11 | `[EDIT: Member 11 Name]` | Pending | `[EDIT: Assigned Module]` | Pending Edit |

---

## 2. Individual Technical Section: File Load and Save

* **Record Schema:** Pipe-delimited lines (`ISBN|Title|Author|Year|TotalCopies|AvailableCopies`).
* **Startup Load:** Parses each line safely on `|`, validates integer conversions, skips empty or malformed lines, and inserts valid records into both the Hash Table and AVL Tree ($O(n \log n)$ total).
* **Sorted Save (Option 11 & Exit):** Traverses the AVL Tree in ascending A–Z title order and rewrites `books.txt` ($O(n)$).

---

## 3. Verification & Boundary-Case Tests (12-Book Dataset)

| Test Case | Input / Condition | Expected & Observed Result |
|---|---|---|
| Startup File Load | `books.txt` with 12 valid records | Prints `Loaded 12 book(s) from books.txt.` |
| Invalid Menu Input | Empty line or `abc` at `Choice:` | Prints `Invalid input: enter a whole number from 0 to 11.` |
| Prefix Search | Option `4`, prefix `clean` | Returns 2 books (*Clean Architecture*, *Clean Code*) |
| Range Search | Option `5`, lower `c`, upper `d` | Returns 6 books in range |
| Ordered AVL Report | Option `10` | Lists 12 titles A–Z; ends with `12 title(s); AVL height 4` |
| Save & Exit | Option `11`, then `0` | Saves all 12 records sorted A–Z by title |
| Boundary: Blank / Malformed Lines | Empty lines or missing `|` fields | Skipped cleanly without crashing |

---

## 4. Reflection & AI Use Declaration

* **Reflection:** Building File Load and Save reinforced how strict input parsing protects in-memory invariants across both the Hash Table and AVL Tree, while AVL in-order saving keeps `books.txt` cleanly sorted.
* **AI Use Declaration:** AI tools (Claude and Gemini) assisted with output verification and document formatting; dataset testing on Kali, code inspection, and final group edits were performed by the student and group.
