### **E-Library Basic Assignment**  
#### **Objective**  
Build a simple **E-Library** web application with a **frontend (React)** and a **backend (FastAPI)** that allows users to view, search, and read books.

---

### **Project Requirements**  

### **1. Frontend (React)**
- **Framework:** React (with React Router)
- **Features:**
  - **Home Page**: Displays a list of books with title, author, and a short description.
  - **Book Detail Page**: Shows full book details, including a "Read Now" button.
  - **Search Functionality**: Search books by title or author.
  - **Read Book Feature**:
    - Open the book in a new page or modal to read.
    - Support for text-based content (can use a PDF viewer or simple text display).
- **Styling**: Use basic CSS or Tailwind CSS.
- **API Integration**: Fetch data from the FastAPI backend using Axios or Fetch API.

---

### **2. Backend (FastAPI)**
- **Framework:** FastAPI (Python)
- **Database:** SQLite or PostgreSQL or MongoDB
- **Features:**
  - **CRUD Operations for Books**:
    - **Create**: Add new books with title, author, and content (text or PDF link).
    - **Read**: Fetch book list and details.
    - **Update**: Modify book details.
    - **Delete**: Remove books.
  - **Search API**: Allow searching books by title or author.
  - **Read Book API**:
    - Provide the book content as text or a PDF link.

- **Endpoints Example:**
  - `GET /books` - Fetch all books
  - `GET /books/{book_id}` - Get book details
  - `POST /books` - Add a new book
  - `PUT /books/{book_id}` - Update book details
  - `DELETE /books/{book_id}` - Delete a book
  - `GET /books/{book_id}/read` - Get book content (text or PDF)

---

### **Bonus (Optional)**
- Add book categories.
- Implement a simple **pagination** for book listings.
- Allow users to **bookmark their progress** in a book.

---

### **Submission Requirements**
- **Code Repository**: Upload the project to GitHub.
- **README.md**: Include setup instructions.
