# 🌈 Grade 1 Learning Hub (Little Steps • Kenya CBC)

A friendly, single-file practice website for Grade 1 learners following the Kenyan Competency Based Curriculum (CBC). Learners pick a subject, read a short lesson, then answer a quick quiz to earn stars and track progress.

> **Note:** This is a starter practice tool, not an official KICD textbook or a guarantee of school results. Always follow the learner's school and the current KICD Grade 1 curriculum for full requirements.

---

## ✨ Features

- **8 subjects** with a short lesson, a worked example, a "Try this" activity, and a practice quiz:
  - 📚 English
  - 🗣️ Kiswahili
  - 🔢 Mathematics
  - 🌱 Environmental Activities
  - 🧼 Hygiene and Nutrition Activities
  - 🎨 Creative Activities
  - 🤸 Movement and Physical Activities
  - 💛 Religious Education
- **Quizzes** with instant, encouraging feedback and a short explanation after every answer
- **Progress tracking**: overall % complete, subjects practised (out of 8), and stars earned
- **Personalised greeting**: optional learner name
- **Weekly routine**: a simple Monday–Friday study plan
- **Grown-up note**: guidance for parents and teachers
- **Responsive design**: works on phones, tablets, and desktops
- **Accessible touches**: visible focus outlines, `aria-live` feedback, and labelled inputs
- **Works offline**: no internet needed once the file is saved

---

## 🚀 Getting Started

No installation, build step, or dependencies required.

1. Download `grade1_learning_hub.html`.
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari).
3. Start learning!

To use it offline on a phone or tablet, save the file to the device and open it from the browser or file manager.

### Hosting (optional)

Because it's one static file, it can be hosted anywhere: GitHub Pages, Netlify, Vercel, or any basic web server. Just upload the HTML file (rename it to `index.html` if you want it to load at the site root).

---

## 🎮 How It Works

1. **Choose a subject** from the card grid.
2. **Read the lesson** together with a grown-up.
3. **Start the practice quiz** and tap an answer for each question.
4. **See your result.** Scoring **60% or higher** marks the subject as practised (⭐ on the card).
5. **Earn stars:** 1 star for every correct answer. Retry any quiz to improve.

### Saving Progress

Progress (subjects practised, stars, best scores, learner name) is stored in the browser's `localStorage` under the key `littleStepsGrade1_v1`.

- Progress stays **on the device and browser** being used. It doesn't sync across devices.
- Clearing browser data will remove it.
- Use the **Reset progress** button to clear stars and subject progress (the learner's name is kept).

---

## 🗂️ Project Structure

```
grade1_learning_hub.html   # The entire app: HTML + CSS + JavaScript
README.md                  # This file
```

Inside the HTML file:

| Section | Purpose |
| --- | --- |
| `<style>` | All styling, with CSS variables for colours and responsive breakpoints at 700px and 420px |
| `<body>` | Hero header, stats, subject grid, lesson/quiz panel, weekly routine |
| `<script>` | The `subjects` data array plus lesson, quiz, and progress logic |

---

## ✏️ Customising Content

All lessons and quiz questions live in the `subjects` array at the top of the `<script>` block. To edit a subject or add a new one, follow this shape:

```js
{
  id: "english",                    // unique ID
  name: "English",                  // card title
  emoji: "📚",                      // card icon
  desc: "Short card description",
  topic: "Lesson topic",
  lesson: "Lesson text shown to the learner.",
  example: "c • a • t  →  cat",     // big highlighted example
  tip: "A hands-on 'Try this' activity.",
  questions: [
    {
      q: "Question text?",
      opts: ["Option A", "Option B", "Option C", "Option D"],
      a: 0,                         // index of the correct option (0 = first)
      why: "Explanation shown after answering."
    }
  ]
}
```

Progress totals, the progress bar, and the subject cards update automatically based on the array length.

**Other easy tweaks**

- **Colours:** edit the CSS variables in `:root` (e.g. `--blue`, `--yellow`).
- **Pass mark:** change `0.6` in the `finishQuiz()` function.
- **Weekly routine:** edit the `.schedule` block in the HTML.
- **Storage key:** change the `STORE` constant (this also resets everyone's saved data).

---

## ⚠️ Known Limitations

- The **"Daily learning goal (minutes)"** stat is a fixed display value (10), not a live streak or timer.
- Progress is local to one browser and device, and there are no user accounts.
- Content is a small starter set (3–4 questions per subject) and is not a full curriculum.
- Quizzes can't be adjusted by difficulty, and there's no audio or read-aloud support yet.

## 💡 Ideas for Future Improvements

- Audio read-aloud for lessons and questions
- More questions per subject, randomised order
- Real daily streak tracking
- Printable worksheets and progress certificates
- Multiple learner profiles on one device
- Additional language support

---

## 👩‍👧 For Parents and Teachers

- Sit with the learner and read the instructions aloud.
- Practise with real objects, songs, drawing, and conversation. Short, happy sessions work better than cramming.
- Ask the learner's teacher which topics are being covered in class.

---

## 📄 License

Add your preferred license here (e.g. MIT) before sharing or publishing.
