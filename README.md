# 🚦 Procurement Logic Capturer

A dynamic Streamlit application for capturing and managing procurement business logic with geography and category hierarchies.

## 🚀 Quick Start - Run on Localhost

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Step-by-Step Instructions

1. **Open Terminal/Command Prompt**
   - On macOS/Linux: Open Terminal
   - On Windows: Open Command Prompt or PowerShell

2. **Navigate to the project directory**
   ```bash
   cd /Users/safarisaev/Projects/ORO_Logic
   ```

3. **Create a virtual environment (recommended)**
   ```bash
   python3 -m venv venv
   ```
   
   **Activate the virtual environment:**
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   
   This will install:
   - `streamlit` - Web framework
   - `pandas` - Data manipulation
   - `openpyxl` - Excel file support

5. **Run the application**
   ```bash
   streamlit run app.py
   ```

6. **Access the app**
   - The terminal will show a message like:
     ```
     You can now view your Streamlit app in your browser.
     Local URL: http://localhost:8501
     ```
   - Your browser should automatically open to `http://localhost:8501`
   - If not, manually open your browser and go to `http://localhost:8501`

### 🛑 To Stop the Server
- Press `Ctrl + C` in the terminal

## 📋 Features

- **📊 Scope Configuration**: Select Geography (Region → Cluster/DRBU → End Market) and Categories (L1 → L2 → L3 → L4)
- **⬅️ Stream 1: Buying Channels**: Define supplier pools and marketplace logic
- **➡️ Stream 2: Sourcing Logic**: Configure tactical vs strategic thresholds and routing rules
- **🗺️ Logic Flow Visualization**: Real-time Mermaid.js flow diagrams
- **💾 Export**: Download logic as JSON or Excel files
- **📈 Review & Export**: Generate final output ready for ORO team

## 🎯 Usage Guide

### 1. Scope Selection (Sidebar)
- Select **Region** → **Cluster/DRBU** → **End Market(s)** (multiple selection)
- Select **Business User End Market(s)** (multiple selection)
- Enter or select **Company Code**
- Select **Category** hierarchy: **L1** → **L2** → **L3** → **L4**

### 2. Stream 1: Buying Channels
- Add suppliers with vendor codes and channel types
- Toggle marketplace allowance
- Set marketplace auto-approve limit

### 3. Stream 2: Sourcing Logic
- Set tactical vs strategic threshold
- Configure tactical action (Fairmarkit, 3-Bids, Spot Buy Desk, etc.)
- Configure strategic owner (Global Category Lead, Sourcing Manager, etc.)
- Add SDC/Desk instructions

### 4. Logic Flow Visualization
- View real-time flowchart based on your selections
- Download Mermaid code for sharing

### 5. Final Output
- Click "Generate Logic Output" to create JSON blueprint
- Download as JSON or Excel
- Share with ORO team

## 📦 Dependencies

- `streamlit>=1.28.0` - Web application framework
- `pandas>=2.0.0` - Data manipulation
- `openpyxl>=3.1.0` - Excel file support (optional, for Excel export)

## 🔧 Troubleshooting

### Port Already in Use
If port 8501 is busy, Streamlit will automatically use the next available port (8502, 8503, etc.)

### Module Not Found Error
Make sure you've activated your virtual environment and installed dependencies:
```bash
pip install -r requirements.txt
```

### Excel Export Not Working
If Excel export is disabled, install openpyxl:
```bash
pip install openpyxl
```

## 📁 Project Structure

```
ORO_Logic/
├── app.py                    # Main Streamlit application
├── requirements.txt          # Python dependencies
├── README.md                 # This file
├── geo_master.csv           # Sample geography data (optional)
└── Geographies & Categories.csv  # Sample data file (optional)
```

## 💡 Tips

- The app uses default data if no files are uploaded
- All categories are available for all geographical selections
- The visualization updates in real-time as you fill in Stream 1 and Stream 2
- Use the "Generate Logic Output" button to create the final JSON blueprint

