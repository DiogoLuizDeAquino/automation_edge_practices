## 📂 WF_Web_Form.psw

**Description:** 

Extracts the CSV file that feeds the next workflow with the necessary information for the continuation of the process.

![WF_Web_Form](https://github.com/user-attachments/assets/e15ab12f-b182-484b-be6f-9a625390a398)

---

## 📂 WF_Web_Form_URL.psw

**Description:**

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
---

## 📂 WF_RPA_MAIN_INTEGRA_FORMTABLE.psw

**Description:**

Main process that extracts the CSV file that feeds the next workflow with the necessary information for the continuation of the process and calls the other workflows.

![image](https://github.com/user-attachments/assets/8160a490-6a4b-4d91-8f30-c06d29421d77)

---

## 📂 WF_RPA-WEB_FORM.psw

## Description:

This Automation Edge workflow automates the process of filling out a web registration form on the following website:  
[https://rpanapratica.koden.com.br/.html](https://rpanapratica.koden.com.br/)

---

### ✅ Step-by-Step Description

| Step Name                     | Action                                                                                                                              |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **InsereUsuários** | Reads user data from a source (e.g., a CSV file or database) that contains the information required to fill the form.                 |
| **Stream lookup Get Variables** | Retrieves additional variables or performs lookups to enrich the user data before form submission.                                    |
| **Abre Form** | Launches the web browser and navigates to the registration form URL.                                                                |
| **Startloop Web Composite** | Initiates a loop to process multiple user records. This step suggests that a "Web Composite" component encapsulates the entire form-filling process for each user. |
| **Blocking Step** | Acts as a control point, potentially to pause the workflow for validation or to handle exceptions.                                    |
| **DefineGenero** | Makes a decision based on the gender information of the current user record to select the appropriate gender option on the form.      |
| **DefineGenero2** | Another decision point related to gender, potentially for further validation or handling of different gender-related fields.            |
| **Feminino** | Selects the "Feminino" (Female) option on the web form.                                                                             |
| **Masculino** | Selects the "Masculino" (Male) option on the web form.                                                                              |
| **Estado** | Fills in the "Estado" (State) field on the web form.                                                                                |
| **Pais** | Fills in the "País" (Country) field on the web form.                                                                                |
| **Criar** | Clicks the "Create" or "Submit" button on the form to register the user.                                                            |
| **Delay row** | Introduces a delay or pause after submitting each user's data, allowing the web application to process the submission before proceeding to the next record. |
| **Continue LoopNovoUsuário** | Continues the loop to process the next user record from the input data.                                                               |
| **Exit Browser** | Closes the web browser after all user records have been processed and the automation is complete.                                   |
| **RelacaoEstados** | This step appears to be a parallel or preparatory process that manages or provides data related to "Estados" (States), possibly for validation or as input to "InsereUsuários". |

---

## 📂 WF_RPA-WEB_TABLE.psw

## Description:

This Automation Edge workflow automate the extraction, processing, and organization of data from a web table, likely involving filtering, data manipulation, and output to an Excel file.

---

### ✅ Step-by-Step Description

| Step Name                     | Action                                                                                                                              |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Start Browser** | Launches the web browser to access the web page containing the table.                                                               |
| **EsperaTabela** | Introduces a waiting period, likely to ensure that the web table is fully loaded and visible before attempting to interact with it. |
| **Web Table** | Interacts with or extracts data from a web table on the opened web page. This is the core step for data retrieval.                 |
| **Aguarda Tabela** | Another waiting step, potentially to confirm the table data is stable or fully available after an action.                         |
| **Microsoft Excel Writer** | Writes the extracted or processed data into a Microsoft Excel file. This is an output step.                                         |
| **Exit Browser** | Closes the web browser after all necessary web interactions are completed.                                                          |
| **OrdenaAlfabetica** | Sorts the data alphabetically based on a specific field or column. This step happens after the initial browser interaction and likely processes data already extracted or prepared. |
| **UnificaRepetidas** | Consolidates or merges duplicate records within the dataset, ensuring uniqueness.                                                    |
| **DivideCampoNascimento** | Divides or parses a field containing birth date information into separate components (e.g., day, month, year).                      |
| **Filtra Feminino** | Filters the dataset to include only records where the gender is "Feminino" (Female).                                              |
| **Altera Estado** | Modifies the "Estado" (State) field for certain records. This could be a data transformation or correction step.                   |
| **Filtra Estado** | Filters the dataset based on the "Estado" (State) field, potentially to segregate data by state.                                    |
| **Aguarda Gravacao** | A waiting step, likely to ensure that a previous data recording or writing operation is complete before proceeding.                |
| **TabelaDasSolteiras** | This step likely processes or outputs data specifically related to "single" individuals, possibly after filtering by marital status or a similar criterion. |
| **TabelaDasCasadas** | This step likely processes or outputs data specifically related to "married" individuals, potentially after filtering by marital status. |

![image](https://github.com/user-attachments/assets/eba70c92-f26b-49f6-a0f4-6db0374b2b15)

---
---
---
