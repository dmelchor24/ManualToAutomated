# 🤖 Manual Test Case to Automated Script Converter using Robot Framework
🎯 This project automates the generation of test scripts from manual test cases defined in a .csv file. It is designed to help QA teams accelerate their automation process without needing to write code from scratch.

---

# 📂 What does this application do?
1. 📤 Allows you to upload a .csv file with your test cases.
2. ✅ Validates that the file contains the correct column headers.
3. 🤖 Automatically generates test scripts using Robot Framework.
4. 🗂️ Suggests a modular project structure following the Page Object Model (POM) pattern.

---

# 🧾 `.csv` File Requirements
The file must contain the following headers, written exactly as shown:

| Column                 | Description                         |
| ---------------------- | ----------------------------------- |
| 🆔 `ID`                | Unique identifier for the test case |
| 📛 `Nombre de TC`      | Descriptive name of the test case   |
| 📝 `Descripción de TC` | Short summary of the objective      |
| 🔢 `# Paso`            | Step number                         |
| ⚙️ `Acción`            | Action to perform in the step       |
| 📥 `Datos`             | Input data, if applicable           |
| ✅ `Resultado Esperado` | Expected result to verify           |

> ⚠️ If any column is missing or misspelled, the file will be rejected.

You can find a sample file at:
📄 [`/examples/test_cases_template.csv`](./examples/test_cases_template.csv)

---

# 📁 Suggested Project Structure (Based on POM)
Once the file is processed, the Robot Framework project is recommended to follow this structure:

| Path                 | Description                         |
| ---------------------| ----------------------------------- |
|/tests/               | Test cases organized by functionality |
|/resources/           | Page objects |
|/keywords/            | Reusable keywords |
|/variables/           | Common data, environment, credentials |
|/results/             |Execution reports (output.xml, log.html, report.html) |

---

# 🚀 How to Use the Converter
1. 🔽 Upload your .csv file containing the test cases.
2. 🤖 The system will automatically generate the .robot scripts.
3. 📦 Download the scripts and place them in the recommended project structure.
4. 🧪 Run your tests using the command: `robot tests/`
