# User Card Manager

A simple and interactive **User Card Manager** built with HTML, JavaScript, and Tailwind CSS. The project allows users to enter their details through a form and dynamically creates user profile cards on the page.

## ✨ Features

* Add a new user through a form
* Display user profile cards dynamically
* Add:

  * Name
  * Role
  * Bio
  * Profile photo
* Remove a user by clicking on their card
* Automatically reset the form after adding a user
* Dynamic DOM manipulation using JavaScript
* Modern and responsive UI using Tailwind CSS

## 🛠️ Technologies Used

* **HTML5** – Structure of the application
* **JavaScript** – Application logic and DOM manipulation
* **Tailwind CSS** – Styling and responsive UI

## 📂 Project Structure

```text
User-Card-Manager/
│
├── index.html
├── script.js
└── README.md
```

## ⚙️ How It Works

The project uses a JavaScript object called `userManager` to manage the users.

### Adding a User

When the form is submitted:

1. The default form submission is prevented.
2. The entered user details are collected.
3. A new user object is added to the `users` array.
4. The form is reset.
5. The user cards are rendered again on the page.

Each user is stored as an object containing their name, role, bio, and photo.

```javascript
{
  userName: "Nitin",
  role: "Frontend Developer",
  bio: "Learning and building web projects.",
  photo: "image-url"
}
```

### Removing a User

Clicking on a user card removes that user from the list.

The `removeUser()` method uses `splice()` to remove the selected user and then re-renders the UI.

```javascript
removeUser: function(index) {
    this.users.splice(index, 1);
    this.renderUi();
}
```