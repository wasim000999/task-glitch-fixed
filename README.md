# Task Glitch – Bug Fixes (Erino SDE Assignment)

This repository contains my completed solution for the SDE Internship Assignment provided by Erino.  
The original Task Management Web App had multiple logic, UI, and performance bugs.  
All 5 mandatory bugs have been fixed, the app has been optimized, and the final version is deployed.

---

## 🚀 Live Demo
(Replace this with your Vercel link)

**Live App:** https://task-glitch-fixed-wasim.vercel.app  
**GitHub Repo:** https://github.com/wasim000999/task-glitch-fixed

---

## ✅ Completed Bug Fixes

### 1. ❗ Double Fetch on Page Load (BUG 1)
- Removed duplicated fetch calls.
- Added `useRef` guard (`fetchedRef.current`).
- Deleted the injected second `useEffect` that caused racing and duplicates.

### 2. ❗ Undo Snackbar Bug (BUG 2)
- Fixed stale restore issue.
- Reset `lastDeleted` state after snackbar closes.
- Ensured only the most-recent delete is restored.

### 3. ❗ Unstable Sorting & Flickering (BUG 3)
- Implemented a deterministic stable sorting algorithm:
  - ROI DESC
  - Priority DESC
  - Title alphabetical (tie-breaker)
- Removed random `Math.random()` based reordering.

### 4. ❗ Double Dialog Opening (BUG 4)
- Prevented Edit/Delete buttons from also triggering View dialog.
- Added `e.stopPropagation()` to action buttons.

### 5. ❗ ROI Validation Issues (BUG 5)
- Implemented `safeROI()`:
  - Prevents NaN / Infinity
  - Handles zero or invalid inputs
  - Formats values cleanly
- Eliminated divide-by-zero errors.

---

## ⚙️ Tech Stack
- **React + Vite**
- **TypeScript**
- **Material UI**
- **Context API**
- **Vercel Deployment**

---

## 🛠 How to Run Locally

```bash
npm install
npm run dev
