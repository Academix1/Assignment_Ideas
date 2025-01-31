### **Digital Whiteboard Assignment** 🎨  

#### **Objective**  
Build a **real-time collaborative digital whiteboard** using **React (Frontend)** and **FastAPI (Backend)** that allows multiple users to draw, erase, and interact on a shared canvas.  

---  

## **Project Requirements**  

### **1. Frontend (React + Canvas API)**  
- **Framework:** React with HTML5 Canvas API  
- **Features:**  
  - **Drawing Tools:**  
    - Users can draw using different colors and brush sizes.  
    - Erase tool to remove specific drawings.  
  - **Undo/Redo Functionality:**  
    - Allows users to revert or redo their last drawing actions.  
  - **Clear Board:**  
    - Option to clear the entire whiteboard.  
  - **Save & Export:**  
    - Users can save their drawings as an **image (PNG/JPG)** or **PDF**.  

---

### **2. Backend (FastAPI + WebSockets)**  
- **Framework:** FastAPI (Python)  
- **Database:** MongoDB or PostgreSQL (optional for saving drawings)  
- **Features:**  
  - **Real-Time Synchronization:**  
    - Use WebSockets to update the board instantly for all connected users.  
  - **Store Drawings:**  
    - Save the drawing history in a database.  
  - **Autosave Feature:**  
    - Periodically save the whiteboard state to avoid data loss.  

- **Endpoints Example:**  
  - `GET /board/{room_id}` - Fetch existing board data  
  - `POST /board/save` - Save board data  
  - `DELETE /board/{room_id}` - Clear the board  
  - `WEBSOCKET /ws/board/{room_id}` - Real-time updates for a whiteboard  

---

### **Bonus (Optional)**  
- **Text & Shape Support:** Allow users to add text, lines, rectangles, and circles.  
- **AI-Powered Sketch Recognition:** Convert rough sketches into refined shapes.  

---

### **Submission Requirements**  
- **Code Repository:** Upload the project to GitHub.  
- **README.md:** Include setup instructions and API documentation.  

