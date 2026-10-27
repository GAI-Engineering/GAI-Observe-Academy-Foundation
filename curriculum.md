▸ GAI OBSERVE · ACADEMY

# Foundation Curriculum — The Pointers

**Scope, stated once and honestly:** this curriculum covers Google Colab and Python only as far as the POC Learning Lab notebooks use them, plus the handful of GenAI ideas those notebooks assume. Everything below is our own text. The teaching itself lives in the external courses we point to — take those from their providers.

Work the modules in order. Each one ends with **Pointers**: where to learn it properly.

---

## Module 0 — Start Here: Notebooks and Google Colab

### What to learn

- **What a notebook is.** A notebook is a document that mixes ordinary written text with live code, arranged in *cells*. Text cells explain; code cells run. You run the code cells in order, top to bottom, and each cell's result appears directly underneath it. The document therefore shows the reasoning and the evidence together — which is exactly why our Lab publishes its work as notebooks.
- **Open your first notebook.** Go to Google Colab (link below), sign in with a Google account, and open the "Welcome to Colaboratory" notebook Colab offers you. Read a little of it — it is written to be your first tour.
- **Run a cell.** Click into a code cell and run it (the play button, or Shift+Enter). Change a number in the cell, run it again, and watch the output change. That small loop — change, run, look — is the whole skill this course is built on.
- **Make a notebook of your own.** Create a new notebook, add one text cell saying what you are doing, and one code cell that prints a sentence. 
- **Save your work.** Notebooks in Colab save to your Google Drive (File → "Save a copy in Drive"). Save your practice notebook so you can return to it.

### Why it matters for our Lab

Every POC in the Lab is a notebook. There is no separate app to install and no environment to configure — if you can open Colab, run cells in order, and save a copy, you can run every notebook we publish. Module 4 asks you to do exactly that, on a real Lab notebook.

### Pointers

- **Google Colab** — Google. This is the tool itself; the welcome notebook inside it is the guided first run. → https://colab.research.google.com/

---

## Module 1 — Python Basics

### What to learn

Learn these six things, and only these six things, well enough to *recognise* them in someone else's code:

- **Variables** — names that hold values (`total = 42`), and how a value changes as a program runs.
- **Strings** — text in quotes, how text is joined, split, and searched.
- **Conditionals** — `if / else`: how a program chooses between paths.
- **Loops** — `for` and `while`: how a program repeats an action over a list of things.
- **Functions** — named, reusable blocks of code that take inputs and return results.
- **Lists and dictionaries** — Python's two everyday containers: an ordered list of items, and a set of labelled values (`{"name": ..., "score": ...}`). Most data in our notebooks travels in one of these two shapes.

Then, the skill underneath all six: **reading code written by others — including code an AI assistant wrote.** Read top to bottom, one line at a time, and say in plain words what each line does before moving on. You do not need to be able to write elegant Python. You need to be able to *follow* it.

### Why it matters for our Lab

Open any Lab notebook and the code is these six things plus libraries other people wrote. When a notebook loops over a list of contracts, checks each one against a condition, and stores the verdicts in a dictionary, there is nothing in it beyond this module. Members who finish Module 1 stop seeing Lab code as a wall and start seeing it as sentences.

### Pointers

- **Kaggle Learn — Python** — Kaggle. A short, free, hands-on micro-course that runs in notebooks in your browser — the same medium as our Lab. Its seven lessons map almost exactly onto this module: variables, functions, conditionals, lists, loops, strings and dictionaries, and working with external libraries. About five hours, at your own pace. → https://www.kaggle.com/learn/python
- **Google's Python Class** — Google for Developers. Free written materials, lecture videos, and exercises. Best if you have seen *some* programming before, in any language. → https://developers.google.com/edu/python
- **Python for Everybody** (Specialization, University of Michigan) — Coursera. The slow, thorough, certificate-bearing route, for members who want a complete foundational course rather than a Lab-scoped one. *Search the Coursera catalogue for "Python for Everybody" — enrolment and pricing are Coursera's.*
- **The Python Tutorial** — python.org. The language's official tutorial and reference. Keep it beside you as the place to check "what does this actually do?" while you read Lab code. → https://docs.python.org/3/tutorial/

---

## Module 2 — Coding with an AI Assistant

### What to learn

This module is mostly habit, not syntax:

- **Ask for small pieces.** Ask the assistant for one function, one step, one explanation at a time — never "write the whole thing." Small pieces are pieces you can check.
- **Make it explain itself.** "Explain this code line by line, in plain language" is a legitimate and powerful prompt. If the explanation does not match what you wanted, the code is wrong even if it runs.
- **Never run code you cannot roughly paraphrase.** If you cannot say, in one sentence, what a block of code is about to do, you are not ready to run it. Ask until you can.
- **Read → run → verify.** Read the code. Run it on something small whose answer you already know. Compare what came out with what you expected. Only then trust it on the real input.
- **Treat error messages as information.** An error is the program telling you where it stopped and why, in its own compressed language. Read the last line first, and do not be shy about pasting the whole error back to the assistant and asking what it means.

### Why it matters for our Lab

The Lab's notebooks were built with AI assistance, and the Academy expects you to extend and re-run them the same way. The assistant is a fast, confident, and *unverified* colleague: it will produce plausible code that is subtly wrong, and it will do so politely. Read → run → verify is the Academy's house discipline precisely because our community works this way — it is also why our notebooks label scripted demonstrations INTERIM and pattern figures ILLUSTRATIVE instead of dressing them up as measurements.

### Pointers

- This module is deliberately ours: the habit above is the lesson, and Modules 0–1 give you the ground to practise it on. Practise on your Module 0 notebook — ask an assistant to write a tiny function for it, paraphrase the function back, run it on numbers you can check by hand.
- For background on what these assistants are and how they behave, the first pointer in Module 3 is the right next read.

---

## Module 3 — GenAI in Plain Terms

### What to learn

Four ideas, at concept level only — what they *are*, not how to build them:

- **Large language models (LLMs).** A model trained on very large amounts of text that predicts what text should come next. Everything an LLM does — answering, summarising, drafting code — is that one ability, applied well.
- **Prompts.** The instructions and context you hand the model. The output you get is a function of the prompt you gave; vague prompt, vague answer. Prompting is a communication skill before it is a technical one.
- **Embeddings and RAG.** *Embeddings* turn text into numbers so a computer can judge which pieces of text are *about* similar things. *RAG* (retrieval-augmented generation) uses that trick in a simple pattern: first retrieve the documents relevant to a question, then ask the model to answer using those documents — so the answer is grounded in sources you chose, not only in what the model remembers.
- **Agents.** An LLM placed in a loop: given a goal, it plans a step, uses a tool (search, code, a document), looks at the result, and decides the next step. An agent is not a different kind of model — it is a model given structure, tools, and permission to iterate.

### Why it matters for our Lab

This is the complete conceptual vocabulary the POCs assume. The Lab's proof-of-concepts explore agents that perceive their surroundings, systems that coordinate through conversation, and agents bound by explicit contracts — every one of them is some combination of an LLM, a prompt, retrieval, and a loop. With this module's four ideas, a Lab notebook's opening explanation should read as a plan you recognise, not a spell you admire.

### Pointers

- **Introduction to Generative AI** and **Introduction to Large Language Models** — Google Cloud Skills Boost. Short introductory courses that open Google's Generative AI learning path, written for non-specialists. → Start from the Skills Boost catalogue and search "Generative AI": https://www.cloudskillsboost.google/catalog
- **Machine Learning Crash Course** — Google for Developers. When you want to go one level deeper — how models are trained and evaluated, embeddings, and a dedicated module on large language models — this is Google's own fast-paced introduction, with exercises that run in Colab. Start at its prerequisites and prework page, which is honest about the Python it expects (Module 1 covers what our Lab needs of it). → https://developers.google.com/machine-learning/crash-course/prereqs-and-prework

---

## Module 4 — Reading a POC Learning Lab Notebook

### What to learn

Every Lab notebook follows the same anatomy. Learn to find these parts, in this order:

1. **The market lead.** The notebook opens with the world, not the code: the problem space, the data behind it, and why anyone should care. Read it first — it tells you what question the notebook is answering.
2. **The idea.** The concept being tested, stated plainly — the pattern the POC exists to explore.
3. **The run.** The code cells, executed in order. This is where Modules 0–2 pay off: follow the code, watch each cell's output appear beneath it, and notice where the notebook's claims come from.
4. **The results.** What the run produced, stated next to the run that produced it.
5. **The labels.** Look for the mode labels and take them seriously. **INTERIM** marks a scripted demonstration — the mechanics are real, the outcome is staged to show the pattern. **ILLUSTRATIVE** marks figures that demonstrate a pattern rather than report a measurement. A result only counts as a finding when the notebook shows a complete end-to-end run behind it. Reading the labels correctly *is* reading the notebook correctly.

**Then re-run one yourself, in Colab:**

1. Open the notebook in Google Colab.
2. Run the cells from the top, in order (or use "Run all" and then scroll slowly).
3. Confirm each cell's output matches what the notebook shows.
4. Change one small input — a number, a sentence, a threshold — and re-run from that cell down. Watch which results move and which do not. That difference is the POC's actual lesson.

### Why it matters for our Lab

This module is the point of the whole course. The first four modules exist so that this one is easy: a Lab notebook you can open, follow, re-run, and argue with is a notebook you can actually learn from — and, eventually, one you can improve and hand back to the community.

### Pointers

- There are no external pointers in this module, on purpose. The Lab itself is the material now: pick the earliest POC notebook, work it against the anatomy above, and bring your questions — including the ones the notebook cannot answer — back to the Agentic AI Learning Community.

---

## Where next

- **Want the full foundation?** Take a complete course from its provider — Python for Everybody on Coursera for Python, Google's Machine Learning Crash Course for ML, the Generative AI learning paths on Google Cloud Skills Boost for GenAI. This course pointed at them from the start; it was never a substitute for them.
- **Want the Academy's programmes?** The GPA and AAI tracks described in the Academy orientation package assume exactly the ground covered here. You are standing on it now.

*▸ GAI OBSERVE · ACADEMY — pointers, honestly labelled.*
