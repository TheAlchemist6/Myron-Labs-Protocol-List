### **PROTOCOL: Workspace Cleanup & Optimization**

**Objective:**
Your primary task is to remove temporary files, build artifacts, and unused code components from the workspace.

---
### **Core Principles**

1.  **Safety is Absolute:** If any doubt exists about an item, you **must not** delete it. Escalate it for user confirmation.
2.  **Thoroughness is Mandatory:** A "deep scan" is not optional; it is the **only** standard of operation. A superficial scan is a failure to follow protocol. You must inspect the entire specified scope before making any recommendations.

---
### ⚠️ Critical Exclusions & Scan Directives

* **Do Not Delete:** You **must not** delete essential paths like `node_modules`, `dist`, `build`, `package.json`, etc.
* **Do Not Scan/Traverse:** All scans **must** be configured to explicitly prune and ignore these paths from the very beginning for safety and performance.

---
### **Cleanup Procedure**

You **must** follow these steps in strict sequential order.

**1. Foundational Workspace Scan (Read-Only Mandate)**
**This is the most critical step.** Before any analysis, you **must first** perform a complete, recursive scan of the entire workspace to build a comprehensive index of its contents.

* **Action:** Using your native tools, recursively scan every directory and file. Your scan **must** adhere to the **Scan & Search Directives** by pruning excluded paths.
* **Objective:** Your *only* objective in this step is to gather information.
* **Strict Prohibition:** You are **forbidden** from making any decisions or classifying files during this phase. **Do not proceed to Step 2 until this complete scan is finished.**

**2. Analyze Indexed Files for Cleanup Candidates**
Now, using the complete index from Step 1, you will analyze the files to identify potential cleanup candidates.

* **Pass A: Pattern-Based Scan:** From your index, identify generic temporary files and logs (`*.tmp`, `*.log`, `*.bak`).
* **Pass B: Code-Aware Analysis (Meticulous Detail Required)**
    * **Step 1: Identify All Source Files.** From the index, create a list of all potential source code files (e.g., `*.js`, `*.ts`, `*.py`, `*.jsx`, etc.).
    * **Step 2: Read Every Source File.** You **must** read the contents of every single source file identified in the previous step.
    * **Step 3: Map All Dependencies.** As you read each file, parse its contents to find all `import`, `require`, or other dependency statements to build a complete dependency graph.
    * **Step 4: Identify True Orphans.** Compare the complete list of source files against your dependency graph. Any file that is never imported or called is a candidate for the `CONFIRMATION LIST`.

**3. Vet Candidates & Compile Lists**
Classify every candidate identified in Step 2 into one of two lists.

* **Verification Mandate:** Before finalizing the lists, you must confirm that the analysis in Step 2 was based on a full reading of all non-excluded source code files.
* **DELETE LIST:** Items you are **100% certain** are safe to delete (e.g., `*.tmp` files).
* **CONFIRMATION LIST:** Items you have **any doubt** about. All "orphaned" scripts found during the Code-Aware Analysis **must** go on this list by default.

**4. Execute & Report**
1.  Delete all items on the **DELETE LIST**.
2.  Present the **CONFIRMATION LIST** to the user for permission.
3.  Provide a final, concise summary report.
