### Build an Enhanced Personal Portfolio

**Objective**: Build an enhanced personal portfolio with an enquiry form that connects to a backend API to handle submissions. The backend should be developed using **Python** and **FastAPI**, and it should store the form submissions in a **MySQL** or **MongoDB** database.

---

### **Frontend Requirements:**

1. **Portfolio Sections**:
    - **Home Section**: A welcoming introduction to who you are.
    - **About Section**: A brief biography or professional summary.
    - **Projects Section**: Showcase 3-5 of your best projects with links, descriptions, and visuals.
    - **Skills Section**: A list of your technical skills (e.g., programming languages, frameworks).
    - **Contact Section**: Display your contact information and a call to action.
    
2. **Enquiry Form**:
    - The form should include:
        - **Name** (input field)
        - **Email** (input field)
        - **Message** (textarea field)
    - The form should be styled and responsive.
    - Upon form submission, the data should be sent to the backend.

---

### **Backend Requirements (FastAPI with MySQL/MongoDB):**

1. **Database Integration**:
    - Use **MySQL** or **MongoDB** to store submitted data.
    - **MySQL**: Create a table named `enquiries` with columns for `name`, `email`, and `message`.
    - **MongoDB**: Create a collection named `enquiries` to store the form data.

2. **FastAPI**:
    - Create a backend API to handle form submissions.
    - Expose a `POST` endpoint to accept form data.
    - Validate the data using **Pydantic** models.
    - After receiving the form data, store it in the database (MySQL/MongoDB).
    - Provide a success message upon successful submission.

3. **Optional (for MongoDB)**: If you choose MongoDB, the backend should use **pymongo** to interact with the database.

---

### **Frontend and Backend Communication**:

- When a user submits the enquiry form, the frontend should use **JavaScript** to send a `POST` request with the form data to the backend endpoint.
- The backend should validate the incoming data, store it in the database, and return a response confirming the submission.
- On successful submission, display a confirmation message on the frontend.

---

### **Additional Requirements**:

1. **Responsive Design**: Ensure the portfolio is mobile-friendly and displays correctly across various screen sizes.
2. **Backend Security**: Use appropriate validation and error handling for backend inputs.
3. **Styling**: Ensure the form and portfolio sections are visually appealing and consistent in design.

---

### **Expected Deliverables**:

1. **Frontend**:
    - A responsive **portfolio page** with sections: Home, About, Projects, Skills, and Contact.
    - An interactive **enquiry form** with fields for Name, Email, and Message.
    - **JavaScript** to handle form submission and interaction with the backend.

2. **Backend**:
    - A **FastAPI** server that connects to a **MySQL** or **MongoDB** database.
    - A **POST** endpoint to handle form submissions and store data in the database.
    - Proper validation and error handling for form data.

---

### **Evaluation Criteria**:

1. **Functionality**:
    - Does the portfolio display correctly?
    - Does the enquiry form submit data to the backend successfully?
    - Is the data stored correctly in the database?

2. **Code Quality**:
    - Is the code clean, well-structured, and properly commented?
    - Are the backend and frontend codebases separated logically?

3. **Design and UX**:
    - Is the portfolio visually appealing?
    - Is the form easy to use and understand?
    - Is the design responsive and works across different devices?

---

### **Bonus Points**:
- Implement **form validation** on both the frontend (JavaScript) and backend (FastAPI).
- Add **confirmation emails** or a notification when the enquiry is submitted.
- Deploy the portfolio and backend on a platform like **Heroku** or **AWS**.

---

**Submission Instructions**:
- Submit the source code for both the frontend and backend, along with a brief readme explaining how to run the application locally and how the backend connects to the database.
