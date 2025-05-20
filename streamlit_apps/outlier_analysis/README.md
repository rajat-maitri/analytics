```markdown
# Outlier Analuysis App

This is a ready-to-run **Streamlit app template** for analyzing Outliers data using the Tuva data model and Snowflake. It demonstrates best practices for structuring multipage apps, using shared helper functions, and working with Snowflake credentials securely.

---

## 📋 What This Template Includes

- ✅ **Multipage Streamlit layout** with pages in the `pages/` folder
- ✅ **Snowflake integration** using `.streamlit/secrets.toml`
- ✅ **Visualizations** using Plotly and pandas
- ✅ **Custom styling** via Streamlit’s `markdown()` injection

---

## 🚀 How to Run This App

1. **Navigate to this app’s folder**:

   ```bash
   cd streamlit_apps/outlier_analysis
   ```

2. **(Optional but recommended) Activate your virtual environment**:

   ```bash
   source ../../.venv/bin/activate      # Mac/Linux
   .\\..\\.venv\\Scripts\\activate      # Windows
   ```

3. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up Snowflake credentials** by creating a file:

   ```
   .streamlit/secrets.toml
   ```

   Example contents:

   ```toml
   [snowflake]
   user = "your_username"
   account = "your_account"
   warehouse = "your_warehouse"
   database = "your_database"
   schema = "your_schema"
   authenticator = "externalbrowser"
   ```

5. **Run the app**:

   ```bash
   streamlit run app.py
   ```

6. The app will open in your browser at [http://localhost:8501](http://localhost:8501)

---

## 🛠 Developer Notes

- Common shared function can be stored and imported from `shared/utils/helpers.py` directory.
- Any imports from `shared/` require that you first add the project root to `sys.path`. This is handled at the top of each page using `path_utils.add_repo_to_path(levels_up=3)`.

---

## 📁 Folder Overview

```bash
outlier_analysis/
├── app.py                     # Main entry point for Streamlit application
├── pages/                     # Individual dashboard pages
│   ├── dashboard.py
│   └── dashboard-2.py
├── requirements.txt           # Python dependencies for this app
└── .streamlit/                # Streamlit config and secrets
    └── config.toml
    └── secrets.toml (you create this)
```

---

