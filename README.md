# user-centric-crud

## Notes - req.body is form, req.params is URL

## Example Routing

#### Listings

|HTTP<br>Method|URL<br>Endpoint|Controller<br>Action|Purpose|
|---|---|---|---|
| GET | /books | booksCtrl.index | View all the books submitted by the logged in user |
| GET | /books/all | booksCtrl.allBooks | View all the books regardless of who submitted (use querystring params to perform filtering) |
| GET | /books/:id | booksCtrl.show | View the details of any book |
| GET | /books/new | booksCtrl.new | View a form for submitting a book (be sure to define this route before the show route)|
| POST | /books | booksCtrl.create | Handle the new book form being submitted |
| GET | /books/:id/edit | booksCtrl.edit | View a form for editing a book (restrict to user who submitted the book) |
| PUT | /books/:id| booksCtrl.update | Handle the edit book form being submitted (restrict to user who submitted the book) |
| DELETE | /books/:id| booksCtrl.delete | Delete a book (restrict to user who submitted the book) |
| POST | /books/:id | booksCtrl.addReading | Add the logged in user's _id to a book's userReading array |

#### Applications 

Other examples of embedded resources include:

- Workouts or Exercises (for a workout tracker)
- Books or Progress (for a reading tracker)
- Expenses (for an expense tracker)
- Tasks (for a ToDo/task app)
- Moods (for a mood tracker)
- Grocery list (for a grocery app)
- Study sessions (for a pomodoro app)
- Watched movies (for a movie tracker)
- Adresses (for e-commerce apps)
- Recently Viewed Items (for shopping apps)
- Inventory (for an inventory tracking app)

|HTTP<br>Method|URL<br>Endpoint|Controller<br>Action|Purpose|
|---|---|---|---|
| n/a | n/a | index action | View all the comments for a book - no route needed since comments are embedded and displayed with their book |
| n/a | n/a | show action | Viewing a single comment does not make sense |
| n/a | n/a | new action | The form to add a new comment should be displayed on the book's show view |
| POST | /books/:id/comments | commentsCtrl.create | Handle the new comment form being submitted |
| GET | /comments/:id/edit | commentsCtrl.edit | View a form for editing a comment (restrict to user who submitted the comment) |
| PUT | /comments/:id| commentsCtrl.update | Handle the edit comment form being submitted (restrict to user who submitted the comment) |
| DELETE | /comments/:id| commentsCtrl.delete | Delete a comment (restrict to user who submitted the comment) |


## EMBEDDED SCHEMA APP IDEAS

1. Book Tracker
User model: Stores user details and an array of books.
Embedded schema: Books (title, author, status: "reading", "completed", "wishlist").
Features: Add books, update reading status, remove books, filter by status.
2. Workout Logger
User model: Stores user details and an array of workouts.
Embedded schema: Workouts (exercise name, reps, sets, date).
Features: Log workouts, view history, filter by date.
3. Recipe Journal
User model: Stores user details and an array of recipes.
Embedded schema: Recipes (name, ingredients, instructions, rating).
Features: Add recipes, edit details, search by name or ingredient.
4. Movie Watchlist
User model: Stores user details and an array of movies.
Embedded schema: Movies (title, genre, watch status, rating).
Features: Add movies, mark as watched, rate movies, filter by genre.
5. Daily Mood Tracker
User model: Stores user details and an array of mood entries.
Embedded schema: Mood entries (date, mood, notes).
Features: Log daily mood, view past moods, search by date.
6. Expense Tracker
User model: Stores user details and an array of expenses.
Embedded schema: Expenses (amount, category, description, date).
Features: Add expenses, categorize spending, view spending history.
7. Habit Tracker
User model: Stores user details and an array of habits.
Embedded schema: Habits (name, frequency, completion status).
Features: Track daily habits, mark habits as complete, view progress.

## REFERENCED MODEL APP IDEAS
1. Book Reviews App
User Model: Stores user details.
Referenced Model: Review (book title, review content, rating, user reference).
Features: Users can post reviews for books, edit/delete their own reviews, view all reviews.
2. Workout Logger
User Model: Stores user details.
Referenced Model: Workout (exercise name, reps, sets, weight, date, user reference).
Features: Log workouts, view workout history, filter by exercise type.
3. Recipe Sharing App
User Model: Stores user details.
Referenced Model: Recipe (title, ingredients, instructions, user reference).
Features: Users can add, update, and delete their own recipes, view other users’ recipes.
4. Movie Reviews App
User Model: Stores user details.
Referenced Model: Review (movie title, review content, rating, user reference).
Features: Users can post movie reviews, rate movies, and view all reviews.
5. Journal App
User Model: Stores user details.
Referenced Model: JournalEntry (title, content, date, user reference).
Features: Users can create private journal entries, view past entries.
6. Task Manager
User Model: Stores user details.
Referenced Model: Task (task name, description, due date, completion status, user reference).
Features: Users can add, update, and delete tasks, mark tasks as completed.
7. Budget Tracker
User Model: Stores user details.
Referenced Model: Expense (amount, category, description, date, user reference).
Features: Users can log expenses, view spending history, categorize spending.
8. Social Media Mini-App
User Model: Stores user details.
Referenced Model: Post (content, image URL, timestamp, user reference).
Features: Users can create posts, view posts from other users.
9. Habit Tracker
User Model: Stores user details.
Referenced Model: Habit (name, frequency, completion history, user reference).
Features: Users can create habits, track progress over time.
10. Reading List App
User Model: Stores user details.
Referenced Model: Book (title, author, status: "reading", "completed", user reference).
Features: Users can track books they want to read, mark books as completed.
