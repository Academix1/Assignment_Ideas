
### **E-Library Project**

#### **Project Description**
The **E-Library** is a web application designed to provide users with a seamless experience for viewing, searching, and reading books. It consists of two main components: the **frontend** built with **React** and the **backend** built with **FastAPI**. The application allows users to browse a library of books, view details for each book, and read them online. The **Read Book** feature integrates with **PDF.js** (Mozilla's PDF Viewer API) to render PDF books, ensuring a rich reading experience. PDF.js allows for smooth and efficient viewing of PDF documents directly in the browser.

The backend exposes a RESTful API for managing books, including operations like adding new books, editing existing books, and deleting books. The frontend interacts with the backend via API calls, displaying book lists, details, and providing search functionality for efficient navigation. Users can search for books by title or author, and each book page includes a **"Read Now"** button to open and read the book.

---

### **Project Requirements**

#### **1. Frontend (React)**
- **Framework:** React (with React Router)
- **Features:**
  - **Home Page**: Displays a list of books with title, author, and a short description.
  - **Book Detail Page**: Shows full book details, including a "Read Now" button.
  - **Search Functionality**: Search books by title or author.
  - **Read Book Feature**:
    - Open the book in a new page or modal to read.
    - **PDF.js Integration**: Use **PDF.js** to display PDF content in the browser. The API will allow rendering PDF documents directly on the page for users to read.
  - **Styling**: Use basic CSS or Tailwind CSS.
  - **API Integration**: Fetch data from the FastAPI backend using Axios or Fetch API.

---

#### **2. Backend (FastAPI)**
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
    - For PDF books, provide a URL to the PDF file that can be opened and rendered using PDF.js in the frontend.

- **Endpoints Example:**
  - `GET /books` - Fetch all books
  - `GET /books/{book_id}` - Get book details
  - `POST /books` - Add a new book
  - `PUT /books/{book_id}` - Update book details
  - `DELETE /books/{book_id}` - Delete a book
  - `GET /books/{book_id}/read` - Get book content (text or PDF link)

---

#### **Bonus (Optional)**
- Add book categories.
- Implement a simple **pagination** for book listings.
- Allow users to **bookmark their progress** in a book.

---

### **Submission Requirements**
- **Code Repository**: Upload the project to GitHub.
- **README.md**: Include setup instructions.

---

### **Integration of PDF.js (Mozilla)**
- **PDF.js** will be integrated into the frontend to provide a seamless PDF viewing experience. This allows users to read books in PDF format directly within the browser.
- To integrate PDF.js, follow these steps:
  - Install **PDF.js** using npm:  
    ```bash
    npm install pdfjs-dist
    ```
  - In the **Book Detail Page**, add the necessary code to load and display PDF files using the PDF.js API.
  - Use the `PDFJS.getDocument()` method to load PDF files and render them within a `canvas` element in React.
  - The user can click on the "Read Now" button, which will open the PDF in the embedded viewer.

---
