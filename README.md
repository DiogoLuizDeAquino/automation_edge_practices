## 📂 WF_Web_Form.psw

**Description:** 

Extracts the CSV file that feeds the next workflow with the necessary information for the continuation of the process.

![WF_Web_Form](https://github.com/user-attachments/assets/e15ab12f-b182-484b-be6f-9a625390a398)

---

## 📂 WF_Web_Form_URL.psw

**Description:**

Automates the process of filling out a web registration form on the following website:  
[https://demo.automationtesting.in/Register.html](https://demo.automationtesting.in/Register.html)

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

![image](https://github.com/user-attachments/assets/22e374b3-3519-49b8-a381-2b728cc7bd2b)


---

## 📂 WF_RPA-WEB_FORM.psw

## Description:

This Automation Edge workflow automates the process of filling out a web registration form on the following website:  
[https://rpanapratica.koden.com.br/.html](https://rpanapratica.koden.com.br/)

### ✅ Step-by-Step Description

| Step Name                     | Action                                                                                                                              |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **InsereUsuários** | Reads user data from a source (e.g., a CSV file or database) that contains the information required to fill the form.                 |
| **Stream lookup Get Variables** | Retrieves additional variables or performs lookups to enrich the user data before form submission.                                    |
| **Abre Form** | Launches the web browser and navigates to the registration form URL.                                                                |
| **Startloop Web Composite** | Initiates a loop to process multiple user records. This step suggests that a "Web Composite" component encapsulates the entire form-filling process for each user. |
| **Blocking Step** | Acts as a control point, to pause the workflow for validation or to handle exceptions.                                    |
| **DefineGenero** | Makes a decision based on the gender information of the current user record to select the appropriate gender option on the form.      |
| **DefineGenero2** | Another decision point related to gender, for further validation or handling of different gender-related fields.            |
| **Feminino** | Selects the "Feminino" (Female) option on the web form.                                                                             |
| **Masculino** | Selects the "Masculino" (Male) option on the web form.                                                                              |
| **Estado** | Fills in the "Estado" (State) field on the web form.                                                                                |
| **Pais** | Fills in the "País" (Country) field on the web form.                                                                                |
| **Criar** | Clicks the "Create" or "Submit" button on the form to register the user.                                                            |
| **Delay row** | Introduces a delay or pause after submitting each user's data, allowing the web application to process the submission before proceeding to the next record. |
| **Continue LoopNovoUsuário** | Continues the loop to process the next user record from the input data.                                                               |
| **Exit Browser** | Closes the web browser after all user records have been processed and the automation is complete.                                   |
| **RelacaoEstados** | This step appears to be a parallel or preparatory process that manages or provides data related to "Estados" (States), possibly for validation or as input to "InsereUsuários". 

![image](https://github.com/user-attachments/assets/b14dee46-b0a8-4973-9f92-2017bbdfd4f6)

---

## 📂 WF_RPA-WEB_TABLE.psw

## Description:

This Automation Edge workflow automate the extraction, processing, and organization of data from a web table, involving filtering, data manipulation, and output to an Excel file.

### ✅ Step-by-Step Description

| Step Name                     | Action                                                                                                                              |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Start Browser** | Launches the web browser to access the web page containing the table.                                                               |
| **EsperaTabela** | Introduces a waiting period, to ensure that the web table is fully loaded and visible before attempting to interact with it. |
| **Web Table** | Interacts with or extracts data from a web table on the opened web page. This is the core step for data retrieval.                 |
| **Aguarda Tabela** | Another waiting step, to confirm the table data is stable or fully available after an action.                         |
| **Microsoft Excel Writer** | Writes the extracted or processed data into a Microsoft Excel file. This is an output step.                                         |
| **Exit Browser** | Closes the web browser after all necessary web interactions are completed.                                                          |
| **OrdenaAlfabetica** | Sorts the data alphabetically based on a specific field or column. This step happens after the initial browser interaction and processes data already extracted or prepared. |
| **UnificaRepetidas** | Consolidates or merges duplicate records within the dataset, ensuring uniqueness.                                                    |
| **DivideCampoNascimento** | Divides or parses a field containing birth date information into separate components (e.g., day, month, year).                      |
| **Filtra Feminino** | Filters the dataset to include only records where the gender is "Feminino" (Female).                                              |
| **Altera Estado** | Modifies the "Estado" (State) field for certain records. This could be a data transformation or correction step.                   |
| **Filtra Estado** | Filters the dataset based on the "Estado" (State) field, to segregate data by state.                                    |
| **Aguarda Gravacao** | A waiting step, to ensure that a previous data recording or writing operation is complete before proceeding.                |
| **TabelaDasSolteiras** | This step processes or outputs data specifically related to "single" individuals, possibly after filtering by marital status or a similar criterion. |
| **TabelaDasCasadas** | This step processes or outputs data specifically related to "married" individuals, after filtering by marital status. |

![image](https://github.com/user-attachments/assets/eba70c92-f26b-49f6-a0f4-6db0374b2b15)

---
---
---

# 📂 WF_IntegraPlanilhas.psw

## Description:

This Automation Edge workflow integrates data from multiple spreadsheets, performs data validation, lookups, and generates individualized reports and a summary report, which is then distributed via email.

---

### ✅ Step-by-Step Description

| Step Name                     | Action                                                                                                                              |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Planilha_Extratos** | Reads data from the "Extratos" (Statements) spreadsheet. This is a primary input source for the workflow.                                |
| **Data Validator** | Validates the data read from "Planilha_Extratos" to ensure data integrity and correctness. Any invalid data follows a separate path to a log. |
| **Write to log** | Logs details of any data that failed validation from the "Data Validator" step.                                                     |
| **Stream lookup** | Performs a lookup operation on the incoming data stream, enriching the data with additional information from another source. |
| **Modified Java Script Value**| Executes a JavaScript code snippet to transform or calculate new values based on the data stream, typically after the lookup.         |
| **Planilha_Clientes** | Reads data from the "Clientes" (Clients) spreadsheet. This spreadsheet contains customer-specific information used for filtering or reporting. |
| **Memory Group by** | Groups the processed data in memory based on specified criteria, preparing it for summary reporting.                                  |
| **OutPut_Relatório** | Generates a summary report based on the grouped data. This report consolidates information from all processed data.                  |
| **MAIL-TotalCompras** | Sends an email containing the "OutPut_Relatório" to a designated recipient, summarizing total purchases or similar metrics. |
| **John** | Filters or processes data specifically for "John," indicating the generation of a report or data output related to this specific client. |
| **Gastos_John** | Generates a report or outputs data detailing the expenses or transactions specifically for "John."                                   |
| **Maria** | Filters or processes data specifically for "Maria," indicating the generation of a report or data output related to this specific client. |
| **Gastos_Maria** | Generates a report or outputs data detailing the expenses or transactions specifically for "Maria."                                 |
| **Pedro** | Filters or processes data specifically for "Pedro," indicating the generation of a report or data output related to this specific client. |
| **Microsoft Excel Writer** | Writes data, specifically for "Pedro" in this branch, to a Microsoft Excel file. This is a specific output for "Pedro's" data.        |

![image](https://github.com/user-attachments/assets/9a4cbd5a-85e7-44b6-9f3e-ff25543af9a3)

```
```
```
```
# 📂 WF_OCR_API

## Description:

This Automation Edge workflow demonstrates a common pattern for interacting with a RESTful API, specifically for Optical Character Recognition (OCR), to process data and log the results.

### ✅ Step-by-Step Description

| Step Name                     | Action                                                                                                                              |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Start** | Initiates the workflow execution. This is the entry point for the process.                                                                  |
| **Advanced REST Client** | Sends a request to a RESTful API. Given the workflow name "WF_OCR_API," this step is specifically making an API call to an OCR service. It could be sending an image or document for text extraction. |
| **JSON Input** | Processes the response received from the "Advanced REST Client." This step is configured to parse the API's output, which is expected to be in JSON format. |
| **Write to log** | Records the processed data (likely the OCR results extracted from the JSON input) to a log file or system. This is crucial for monitoring and debugging. |

![image](https://github.com/user-attachments/assets/2d1ad816-8af1-4c7c-9c4d-8ad23a0e69ae)

```
```

# 📂 WF_OCR_tesseract.psw

## Description:

This Automation Edge workflow utilizes the Tesseract OCR engine to extract text from images and subsequently processes the extracted text by splitting it into individual rows.

---

### ✅ Step-by-Step Description

| Step Name                     | Action                                                                                                                              |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Start** | Initiates the workflow execution. This is the entry point for the process.                                                                  |
| **OCR: Tesseract** | Performs Optical Character Recognition (OCR) on an image or file, using the Tesseract engine. This step extracts text from visual elements. |
| **Split field to rows** | Takes the text extracted by the "OCR: Tesseract" step and divides it into multiple rows. This is useful for processing each line of text individually after extraction. |

![image](https://github.com/user-attachments/assets/b014f833-6f71-40a1-9602-72de791c9767)

```
```
