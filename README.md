# MEN-Stack Project Planning Guide

## Notes - req.body is form, req.params is URL, render = views directory

## Project Planning Requirements

You will submit a **public Trello board** that includes the following:

### ✅ **1. MVP User Stories**

> **As a** user, **I want** [feature].


### ✅ **2. Wireframes**
Create wireframes for your app’s **main ejs pages**.
- index.ejs (see all items)
- new.ejs (form to create item)
- show.ejs (item detail page)
- edit.ejs  (form to edit item)

### ✅ **3. ERD (Entity Relationship Diagram)**
Draw an **ERD** showing your app's **models** and how they **connect**.  


---

## **How to Organize Your Trello Board**
Create a Trello board with these lists:

**MVP User Stories** → Each user story is a **card**  
**Wireframes** → Each wireframe is a **card** (drag image into list) 
**ERD** → Add your ERD as a **card** (drag image into list)

---

## **Examples of Each Requirement**

### **Skyrockit: MVP User Stories**
**Applications are __embedded__ in a User model.**
- **As a user, I want to create an application for a job.**
- **As a user, I want to edit my application if I make a mistake.**
- **As a user, I want to delete my application if I change my mind.**
- **As a user, I want to see all my submitted applications.**

**Example ERD**  
<img width="406" alt="Screenshot 2025-02-06 at 4 01 10 PM" src="https://github.com/user-attachments/assets/9194d4a6-47b3-4bf1-9303-264fc207f5bb" />

---

### **Open House: MVP User Stories**
**Listings belong to a User.**
- **As a user, I want to create a listing to sell a house.**
- **As a user, I want to edit my listing details.**
- **As a user, I want to delete a listing when the house is sold.**
- **As a user, I want to see all my listings.**

**Example ERD**  
<img width="558" alt="Screenshot 2025-02-06 at 4 06 33 PM" src="https://github.com/user-attachments/assets/8a6eb739-2da6-4637-97fa-50b34a5fbc2b" />


---

## **Table of RESTful Routes**
| HTTP Method | RESTful Route       | Controller Function |
|------------|---------------------|---------------------|
| GET        | `/resources`         | `index()`          |
| GET        | `/resources/:id`     | `show()`           |
| POST       | `/resources`         | `create()`         |
| PUT        | `/resources/:id`     | `update()`         |
| DELETE     | `/resources/:id`     | `destroy()`        |

Example: If your app tracks **applications**, replace `resources` with `applications`.

---

## **Ideas for Simple CRUD Apps**
- **Users & Applications** (Users apply for jobs)
- **Users & Listings** (Users list items for sale)
- **Users & Bookmarks** (Users save favorite articles)
- **Users & Events** (Users create and manage events)

---

## **Stretch Goal User Stories**
- **As a user, I want to favorite/bookmark a [resource].**
- **As a user, I want to filter/sort my [resources].**
- **As a user, I want to upload an image for my [resource].**
- **As a user, I want to search for [resources].**
- **As an admin, I want to delete inappropriate [resources].**

✅ These are **optional** but add extra value to your project.

---

🔗 **Links to Past Student Examples:** [Insert links here]  

Good luck! 🚀
