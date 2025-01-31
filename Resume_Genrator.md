
## **Resume Generator Application with Geolocation Tracking**

### **Objective**:
Build a dynamic resume generator application that allows users to input their details via a form, generate a resume based on their inputs, and store the data in a backend database. The backend should be developed using **Python** and **FastAPI** (or **Flask**), and the data should be stored in a **MySQL** or **MongoDB** database. The generated resume should be displayed in a pre-designed template and available for download as a PDF. Additionally, integrate **IPStack API** to auto-track the user’s geolocation.

---

### **Frontend Requirements**:

1. **Resume Form**:
    - Include fields for:
        - **Personal Information**: Name, Email, Phone Number, Address (auto-filled using IPStack API), and Profile Picture upload.
        - **Objective**: A short paragraph about career goals.
        - **Education**: Degrees, institutions, and achievements.
        - **Work Experience**: Company name, job title, and responsibilities.
        - **Skills**: Technical and soft skills.
        - **Projects**: Descriptions and links.
        - **References** (optional): Name, position, and contact details.

2. **Form Styling**:
    - Use **CSS** or a framework like **Bootstrap/Tailwind CSS**.
    - Ensure the form is responsive and mobile-friendly.
    - Include validation for required fields.

3. **Resume Generation**:
    - Allow users to generate resumes in **PDF format** after submission.
    - Display resumes on the webpage and provide a **download** option.
    - Offer **multiple resume templates** for selection.

4. **Resume Template Options**:
    - **Template 1**: One-page simple layout.
    - **Template 2**: Two-column layout with a focus on skills/projects.
    - **Template 3**: A comprehensive design with all sections.

---

### **Backend Requirements (FastAPI with MySQL/MongoDB)**:

1. **Database Integration**:
    - **MySQL**: Table `resumes` storing form data.
    - **MongoDB**: Collection `resumes` for user form data.

2. **FastAPI/Flask Backend**:
    - Expose a **POST** endpoint for form submission.
    - Validate and store data using **Pydantic** (FastAPI) or **WTForms** (Flask).
    - Generate **PDF resumes** dynamically.

3. **Resume Generation (Backend)**:
    - Use **WeasyPrint, ReportLab, or FPDF** for PDF generation.
    - Ensure formatting aligns with selected templates.

4. **Geolocation Tracking (IPStack API)**:
    - **Task**:
        - Use **IPStack API** to auto-detect and pre-fill the user’s location in the **Address** field.
        - Fetch **City, Region, Country**, and insert them into the form.
        - Example API call:
          ```python
          import requests
          API_KEY = "your_ipstack_api_key"
          response = requests.get(f"http://api.ipstack.com/check?access_key={API_KEY}")
          location_data = response.json()
          print(location_data["city"], location_data["region_name"], location_data["country_name"])
          ```
        - Implement this feature to **enhance user experience** by reducing manual input.

---

### **Frontend and Backend Communication**:

- The frontend should send a **POST** request with form data.
- The backend should:
    - Validate and store the data.
    - Auto-fetch geolocation from **IPStack API**.
    - Generate a resume in the selected template.
    - Provide a **download link** to the user.

---

### **Additional Features**:

1. **Responsive Design**: Ensure compatibility across devices.
2. **PDF Formatting**: Ensure resume sections are properly structured.
3. **Backend Security**: Prevent SQL injection and invalid requests.

---

### **Expected Deliverables**:

1. **Frontend**:
    - A **responsive form** for resume creation.
    - Auto-filled **location** using **IPStack API**.
    - **Multiple resume templates** for selection.

2. **Backend**:
    - A **FastAPI/Flask** backend storing resume data.
    - **PDF generation** with formatting.
    - **IPStack API integration** for location tracking.

---

### **Evaluation Criteria**:

1. **Functionality**:
    - Form submission and database integration.
    - Correct PDF resume generation and download.
    - Proper integration of **IPStack API** for geolocation tracking.

2. **Code Quality**:
    - Clean, well-documented, and modular code.

3. **Design and UX**:
    - User-friendly interface with an elegant layout.

---

### **Bonus Points**:
- Implement **client-side validation** before form submission.
- Allow users to **edit and update** their resumes.
- Deploy on **Heroku, AWS, or Vercel**.

---

### **Submission Instructions**:
- Submit the **source code** (Frontend + Backend).
- Include a **README** explaining:
    - How to run the app.
    - How to set up the database.
    - How the backend handles PDF generation.
    - IPStack API integration details.

---
