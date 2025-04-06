# Image Analysis Module Setup

This is a minimal guide to setting up and testing the image analysis module.

## Dependencies

The module requires these exact versions to ensure compatibility:

```
google-generativeai>=0.3.1
pydantic-settings>=2.0.0
python-dotenv>=1.0.0
requests>=2.28.0
```

## Setup Instructions

### 1. Extract the module

```bash
unzip image_analysis_module.zip
cd image_analysis_module
```

### 2. Set up environment

Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API key

Create a `.env` file in the root directory:
```bash
echo "GOOGLE_API_KEY=your-api-key-here" > .env
```

## Testing

Run the minimal test to verify functionality:
```bash
python direct_test.py
```

This tests only the core functionality, following the minimalist implementation and testability focus.

## Installation in Other Projects

To use as a package in other projects:
```bash
pip install -e /path/to/image_analysis_module
```

Then import:
```python
from image_analysis import analyze_image
```

## Troubleshooting

If the test fails, check:
1. API key is valid
2. Internet connection is working
3. Dependencies are correctly installed
