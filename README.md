# MEN-Stack Project Planning Guide

## Project Planning Requirements

You will submit a **public Trello board** that includes the following:

### ✅ **1. MVP User Stories 🙋‍♀️**


### ✅ **2. Wireframes 🖥️**
Create wireframes for your app’s **main ejs pages**.
- index.ejs (see all items)
- new.ejs (form to create item)
- show.ejs (item detail page)
- edit.ejs  (form to edit item)

### ✅ **3. ERD (Entity Relationship Diagram) ↔️**
Draw an **ERD** showing your app's **models** and how they **connect**.  

---

## **Examples of Each Requirement**

### User Stories 🙋‍♀️

**Skyrockit User Stories: Applications are __embedded__ in a User model.**
- **As a guest, I want to be able to sign up.**
- **As a user, I want to sign into my account.**
- **As a user, I want to create an application for a job.**
- **As a user, I want to see all my submitted applications.**
- **As a user, I want to edit my application if I make a mistake.**
- **As a user, I want to delete my application if I change my mind.**

**Open House User Stories: Listings belong to a User.**
- **As a guest, I want to be able to sign up.**
- **As a user, I want to sign into my account.**
- **As a user, I want to create a listing to sell a house.**
- **As a guest, I want to see everyone's listings.**
- **As a user, I want to see all my listings.**
- **As a user, I want to edit my listing details.**
- **As a user, I want to delete a listing when the house is sold.**

---

### Wireframes 🖥️

<img width="1014" alt="Screenshot 2025-02-06 at 4 50 21 PM" src="https://github.com/user-attachments/assets/6588c834-a61c-440f-801b-930fc6bd844d" />



---

### Example ERDS ↔️
<img width="406" alt="Screenshot 2025-02-06 at 4 01 10 PM" src="https://github.com/user-attachments/assets/9194d4a6-47b3-4bf1-9303-264fc207f5bb" />

<img width="558" alt="Screenshot 2025-02-06 at 4 06 33 PM" src="https://github.com/user-attachments/assets/8a6eb739-2da6-4637-97fa-50b34a5fbc2b" />


---

## **Table of RESTful Routes**
| HTTP Method| RESTful Route          | Controller Function       |
|------------|------------------------|---------------------------|
| GET        | `/resources`           | `myCtrl.index()`          |
| GET        | `/resources/new`       | `myCtrl.newResource()`    |
| POST       | `/resources`           | `myCtrl.create()`         |
| GET        | `/resources/:id`       | `myCtrl.show()`           |
| DELETE     | `/resources/:id`       | `myCtrl.destroy()`        |
| GET        | `/resources/:id/edit`  | `myCtrl.edit()`           |
| PUT        | `/resources/:id`       | `myCtrl.update()`         |


Example: If your app tracks **applications**, replace `resources` with `applications`.

---

## Project Ideas (Simple CRUD Apps)

Here are some ideas for projects where a **user owns many** of **one resource**:

- **Book Tracker:** Users save books to read or review.
  - User model fields: username, password
  - Book model fields: title, author, status: "reading", "completed", "wishlist"
- **Workout Logger:** Users save workout history.
  - User model fields: username, password
  - Workout model fields: exercise name, reps, sets, date
- **Task Manager:** Users create tasks.
  - User model fields: username, password
  - Task model fields: task name, description, due date, completion status
- **Journal App:** Users create journal entries.
  - User model fields: username, password
  - JournalEntry model fields: title, content, date
- **Budget Tracker:** Users log (save) expenses.
  - User model fields: username, password
  - Expense model fields: amount, category, description, date
- **Social Media Mini-app:** Users create text or image posts.
  - User model fields: username, password
  - Post model fields: content, image URL
- **Habit Tracker:** Users track habits.
  - User model fields: username, password
  - Habit model fields: name, frequency, completion history
- **Movie Watchlist:** Users save watched movies.
  - User model fields: username, password
  - Movie model fields: title, genre, watch status, rating
- **Event Planner:** Users create and manage events
  - User model fields: username, password
  - Event model fields: description, category, date, attendees
- **Daily Mood Tracker:** Users create and manage events
  - User model fields: username, password
  - Mood model fields: date, mood, notes

---

## **Stretch Goal User Stories**
- **As a user, I want to favorite a [resource].**
- **As a user, I want to upload an image for my [resource].**
- **As a guest, I want to change the site to dark mode.**
- **As a user, I want to add a comment to a [resource].**
- **As a user, I want to search for [resources].**

These are **optional** but add extra value to your project.

---

🔗 **Links to Past Student Examples:** [Insert links here]  

Good luck! 🚀
