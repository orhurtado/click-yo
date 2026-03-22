# Click-YO

**Click-YO** is a real-time classroom participation system that allows students to join a participation queue, evaluate their peers, and earn medals based on their contributions. Teachers can manage classes, groups, and view voting statistics.

## Features

### 👨‍🏫 For Teachers (`admin.html`)
- Google Authentication for secure access
- Create, edit, and delete classes
- Manage dynamic groups per class
- Open/close participation queue
- Open/close student registration
- Real-time voting dashboard with averages
- Track which students haven't voted yet
- Export voting data and participation medals to CSV
- Restore previous session after page reload

### 📚 For Students (`index.html`)
- Google Authentication
- Register in multiple classes with name and surname
- Select from available groups created by the teacher
- Join the real-time participation queue with one click (¡YO! button)
- View your position in the queue
- Evaluate peers using a 5-criteria rubric (1-5 scale)
- Earn medals (🍋, 🥉, 🥈, 🥇, 💎) for participation
- View the leaderboard of top contributors
- Switch between enrolled classes
- Exit current class to select another

### 🔐 Teacher Authorization (`main.html`)
- Password-protected panel
- Authorize new teachers with name, surname, and email
- Enable/disable teacher access
- Remove teachers from the system

## Tech Stack

- **Frontend**: HTML5, Tailwind CSS, Vanilla JavaScript
- **Backend**: Firebase Authentication, Firestore Database
- **Real-time**: Firestore listeners for live updates

## Firebase Structure
click-yo/
├── clases/
│ └── {claseID}/
│ ├── estudiantes/
│ │ └── {alumnoUID}/ # name, surname, team, medals, points
│ ├── grupos/
│ │ └── {grupoID}/ # group name, creation date
│ └── cola/
│ └── {alumnoUID}/ # student in participation queue
├── votaciones/
│ └── {horario}{team}{voterUID}/ # votes, rubric scores, comments
├── autorizados/
│ └── {email_profesor}/ # teacher authorization data

text

## Installation

1. Clone the repository
2. Create a Firebase project
3. Enable Authentication (Google Sign-In)
4. Create Firestore Database
5. Update `firebaseConfig` in all HTML files with your project credentials
6. Deploy or run locally with a local server

## Usage

1. **First time**: Access `main.html` (default password: `admin2026`) to authorize teachers
2. **Teachers**: Log in via `admin.html` with Google, create classes and groups
3. **Students**: Log in via `index.html` with Google, select a class and team, then participate

## File Structure
├── index.html # Student dashboard
├── admin.html # Teacher dashboard
├── main.html # Teacher authorization panel
├── README.md # Project documentation
└── LICENSE # MIT license

text

## License

This project is licensed under the **MIT License**.
MIT License

Copyright (c) 2026 OHM (Ing.Oscar Hurtado Morato)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
## Credits

**SYSTEM BY OHM** (c) 2026  
Version 3.0 Rev.0

---

*Made with ❤️ for better classroom participation*# click-yo
