---

## **Resume Generator Application with Geolocation Tracking**

**Objective**: Build a dynamic resume generator application that allows users to input their details via a form, generate a resume based on their inputs, and store the data in a backend database. The backend should be developed using **Python** and **FastAPI** (or **Flask**), and the data should be stored in a **MySQL** or **MongoDB** database. The generated resume should be displayed in a pre-designed template and available for download as a PDF. Additionally, integrate **IPStack API** to auto-track the user's geolocation.

### **Frontend Requirements:**

1. **Resume Form**:
    - The form should include the following sections:
        - **Personal Information**: Name, Email, Phone Number, Address, and Profile Picture upload.
        - **Objective**: A short paragraph about the user's career goals.
        - **Education**: List of degrees, institutions, dates, and any special achievements.
        - **Work Experience**: Company name, job title, duration, and responsibilities.
        - **Skills**: A list of technical and soft skills.
        - **Projects**: List of personal or professional projects with descriptions and links.
        - **References** (optional): Name, position, company, and contact details.

2. **Form Styling**:
    - Use **CSS** or a **CSS framework** (Bootstrap, Tailwind CSS) to style the form.
    - Ensure the form is responsive and mobile-friendly.
    - Provide proper validation for required fields (e.g., email, name, etc.).

3. **Resume Generation**:
    - After form submission, the user should be able to generate a resume in PDF format.
    - The resume should be displayed directly on the webpage or made available for download.
    - Provide multiple **resume templates** (e.g., one-page, two-column, minimalistic, professional).

4. **Resume Template Options**:
    - Provide at least **3 pre-designed templates** that the user can choose from:
        - **Template 1**: Simple one-page layout with basic information.
        - **Template 2**: Two-column layout with a focus on skills and projects.
        - **Template 3**: A more comprehensive design with space for objectives, education, work experience, and references.
    - Each template should be selectable on the frontend (e.g., radio buttons or a drop-down list).

---

### **Backend Requirements (FastAPI with MySQL/MongoDB):**

1. **Database Integration**:
    - Use **MySQL** or **MongoDB** to store the form data.
    - **MySQL**: Create a table named `resumes` with columns for all the form fields (e.g., name, email, phone, education, work experience).
    - **MongoDB**: Create a collection named `resumes` to store the user form data.

2. **FastAPI/Flask**:
    - Create a backend API to handle form submissions and resume generation.
    - Expose a **POST** endpoint to accept form data.
    - Validate the data using **Pydantic** (FastAPI) or **WTForms** (Flask).
    - Save the form data into the database (MySQL/MongoDB).
    - Based on the selected template, generate a **PDF** resume.

3. **Resume Generation (Backend)**:
    - Use libraries like **WeasyPrint**, **ReportLab**, or **FPDF** to generate a PDF version of the resume based on the submitted data.
    - After form submission, allow the user to download the generated resume in their chosen template format.

4. **Template Integration**:
    - Implement dynamic generation of the resume using the data submitted via the form.
    - Each resume should follow a pre-designed template selected by the user.
    - Ensure that the generated PDF is styled to match the chosen template.

---

### **IPStack API Integration for Geolocation Tracking:**

1. **Geolocation Auto-Fill**:
    - Use **IPStack API** to auto-detect and populate the user's current location.
    - **Task**:
        - Fetch the user’s IP address and use the IPStack API to retrieve location details.
        - Auto-fill the **Address** field in the resume form with city, state, and country.
        - Provide an option for users to modify the auto-filled address if needed.

---

### **Frontend and Backend Communication**:

- The frontend should send a **POST** request with the form data to the backend API.
- The backend should validate the data, store it in the database, and generate the resume in the selected template.
- Once the resume is generated, provide a **download link** to the user for their personalized PDF resume.

---

### **Additional Requirements:**

1. **Responsive Design**: Ensure the application is mobile-friendly and works across different devices.
2. **Multiple Template Options**: Allow users to select between different templates for their resume.
3. **PDF Formatting**: Ensure that the generated PDF follows the selected template, with all the sections like **Personal Info**, **Objective**, **Work Experience**, etc.
4. **Backend Security**: Validate form data to avoid issues like SQL injection or malformed requests.

---

### **Expected Deliverables:**

1. **Frontend**:
    - A **responsive resume generator form** with fields for Personal Information, Education, Work Experience, Skills, Projects, and References.
    - Options to choose between **multiple resume templates**.
    - A mechanism to **submit** the form data via JavaScript or **Axios** and **display** or **download** the generated resume.

2. **Backend**:
    - A **FastAPI/Flask** server connected to a **MySQL** or **MongoDB** database.
    - A **POST** endpoint to handle form submissions and save the data in the database.
    - Integration with **IPStack API** for geolocation tracking.
    - Dynamic generation of resumes based on the chosen template.

3. **Geolocation Integration**:
    - Documentation on how the **IPStack API** is integrated into the application.
    - Code snippets or examples demonstrating API usage.

---

### **Evaluation Criteria:**

1. **Functionality**:
    - Does the form submit data correctly and store it in the database?
    - Is the resume generated correctly and displayed or made available for download in the chosen template?
    - Does the PDF have the correct formatting and sections as per the selected template?
    - Is the IPStack API correctly fetching and populating the user's location?

2. **Code Quality**:
    - Is the code clean, well-structured, and commented?
    - Is the frontend and backend codebase organized effectively?

3. **Design and UX**:
    - Is the resume generator application easy to use and navigate?
    - Does the application have an aesthetically pleasing design?
    - Is the generated resume easy to read and professional in appearance?

---

### **Bonus Points**:
- Implement **client-side validation** to check the form inputs before submitting.
- Add the ability for users to **save their resume** to the database and later retrieve or update it.
- Allow users to **choose custom templates** in addition to the pre-designed ones.
- **Deploy** the application on platforms like **Heroku**, **AWS**, or **Vercel**.

---

**Submission Instructions**:
- Submit the source code for both the frontend and backend, along with a **readme** explaining how to run the application locally, how to set up the database, and how the backend handles the PDF resume generation.
- Include documentation on how the **IPStack API** is used and configured.

---

