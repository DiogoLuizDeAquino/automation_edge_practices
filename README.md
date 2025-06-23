## 📂 WF_Web_Form.psw

**Description:**  
Extracts the CSV file that feeds the next workflow with the necessary information for the continuation of the process.

![WF_Web_Form](https://github.com/user-attachments/assets/e15ab12f-b182-484b-be6f-9a625390a398)

---

## 📂 WF_Web_Form_URL.psw

### 📋 Purpose

Automates the process of filling out a web registration form on the following website:  
[https://demo.automationtesting.in/Register.html](https://demo.automationtesting.in/Register.html)

---

### ✅ Step-by-Step Description

| Step                          | Action                                                                                          |
|-------------------------------|-------------------------------------------------------------------------------------------------|
| **InsereCSV**                 | Reads data from a CSV file containing user information for the form.                           |
| **Get Variables**             | Retrieves environment variables or workflow parameters.                                         |
| **Start Browser**             | Launches the web browser to begin automation.                                                   |
| **Start Loop**                | Starts a loop to process each record from the CSV file.                                         |
| **Preencher_Form**            | Fills in the personal details fields of the web form (e.g., first name, last name, address, etc.). |
| **Define_Genero**             | Makes a gender-based decision to select the correct gender field.                               |
| **Feminino / Masculino**      | Selects the appropriate gender option on the web form.                                          |
| **Hobbies / Hobbies2 / Hobbies3** | Defines the user's hobbies for selection.                                               |
| **Selec_Hobb / Selec_Hobb2 / Selec_Hobb3** | Clicks or selects the defined hobbies on the web form.                        |
| **Skills**                    | Fills in the "Skills" field on the web form (e.g., Java, Python, etc.).                        |
| **Delay Row**                 | Adds a wait or pause between each loop iteration.                                               |
| **Continue Loop**             | Proceeds to the next iteration to handle the next CSV record.                                   |
| **Blocking Step**             | Acts as a control point to stop or validate the flow if needed.                                 |
| **Exit Browser**              | Closes the web browser after completing all records.                                            |

![WF_Web_Form_URL](https://github.com/user-attachments/assets/3fcb488c-a4f9-4f1d-9800-ecd90ae60755)

---
---
