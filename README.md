

#  ITPU Course Materials

### Teaching resources, lecture notes, labs & assignments
**IT Park University (ITPU) · Fergana, Uzbekistan**

*Maintained by Dilrabo Khidirova — Senior Lecturer in Machine Learning*

[![License](https://img.shields.io/badge/License-MIT-lightgrey.svg)](./LICENSE)
[![Made with Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)](https://www.markdownguide.org/)
![Maintained](https://img.shields.io/badge/Maintained-yes-brightgreen.svg)
![Courses](https://img.shields.io/badge/Courses-3-blue.svg)



---

##  About

This repository is a single, well-structured home for the three undergraduate
courses I teach at ITPU. Every course contains its own syllabus, lecture-by-lecture
materials, hands-on labs, assignments, and curated resources — all version-controlled
and openly organized so that students, colleagues, and collaborators can navigate
them easily.

The goal is a **reproducible, professional, and continuously improving** set of
teaching materials that reflects modern, interactive, and applied approaches to
computer science and machine learning education.

---

##  Courses

| # | Course | Level | Status |
|---|--------|-------|--------|
| 01 | [Introduction to Specialty](./courses/01-introduction-to-speciality/) | Year 1 | 🟢 Active |
| 02 | [Introduction to Digital Technologies](./courses/02-introduction-to-digital-technologies/) | Year 1 | 🟢 Active |
| 03 | [Introduction to Machine Learning](./courses/03-introduction-to-machine-learning/) | Year 2 | 🟢 Active |

Each course folder follows the same predictable layout — see
[Repository Structure](#-repository-structure).

---

## 🗂 Repository Structure

itpu-course-materials/
├── courses/
│ ├── 01-introduction-to-speciality/
│ ├── 02-introduction-to-digital-technologies/
│ └── 03-introduction-to-machine-learning/
│ ├── README.md # Course overview & navigation
│ ├── syllabus/ # Full syllabus, schedule, grading
│ ├── lectures/ # One file per lecture
│ ├── labs/ # Hands-on practical sessions
│ ├── assignments/ # Homework, projects, rubrics
│ ├── resources/ # Readings, links, datasets
│ └── assets/ # Images, diagrams, slides
├── docs/ # Teaching philosophy, facilitator guide, templates
├── shared-resources/ # Material reused across courses
├── assets/ # Repo-wide images
├── scripts/ # Helper scripts (optional)
└── .github/ # Issue & PR templates


---

##  How to Navigate

- **Students** → open the course you're enrolled in, start with its `README.md`,
  then read the `syllabus/`.
- **Each lecture** lives in `lectures/` with notes, examples, and links to
  interactive tools.
- **Labs & assignments** are numbered to match the lecture schedule.

---

##  Teaching Approach

These courses are designed around **active, interactive learning**. Each session
combines:

- Clear objectives and a recap at the start
- Visual teaching aids (slides, infographics, diagrams)
- Live interactive demos and hands-on coding
- Real-world, locally relevant examples
- Open discussion, Q&A, and an end-of-session summary

See [`docs/facilitator-guide.md`](./docs/facilitator-guide.md) for the full
facilitation framework, and [`docs/teaching-philosophy.md`](./docs/teaching-philosophy.md)
for the principles behind it.

---

##  Getting Started (for contributors)

New materials follow shared templates in [`docs/templates/`](./docs/templates/):

1. Copy the relevant template (`lecture-template.md`, `lab-template.md`, or
   `assignment-template.md`).
2. Place it in the correct course folder and fill in every section.
3. Link it from that course's `README.md`.

See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for branch naming and commit conventions,
and [`docs/SETUP-GITHUB.md`](./docs/SETUP-GITHUB.md) for repository setup.

---

## 📄 License

Course materials are released under the [MIT License](./LICENSE) unless stated
otherwise. Third-party materials (datasets, images, referenced papers) remain under
their own respective licenses.

---

## Author

**Dilrabo Khidirova**
Senior Lecturer in Machine Learning · IT Park University (ITPU), Fergana, Uzbekistan

ML Engineer & AI Researcher — trustworthy & explainable AI, uncertainty
quantification, calibration-aware model selection, and low-resource language
fairness. Advocate for women in tech in Central Asia.

