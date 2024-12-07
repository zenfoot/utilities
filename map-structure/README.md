# Directory Structure Mapper

## Overview
A Python utility that analyzes and visualizes directory structures. This tool creates comprehensive reports, visual tree representations, and optional mirror structures of any directory system.

## Prerequisites
- Python 3.x
- Read permissions for the directory you want to analyze

## Installation
1. Download `map_structure.py`
2. No additional dependencies required

## Features
- Complete directory analysis
- Tree-style visualization
- Detailed file type reporting
- Optional mirror structure creation
- Customizable ignore patterns
- UTF-8 encoded output

## Usage

### Basic Commands
```bash
# Analyze current directory
python map_structure.py

# Analyze specific directory
python map_structure.py --input /path/to/analyze

# Custom output location
python map_structure.py --output ./my_analysis

# Create mirror structure
python map_structure.py --input /path/to/analyze --mirror
```

### Command Line Options
- `--input` or `-i`: Source directory path (defaults to current directory)
- `--output` or `-o`: Output location (defaults to ./structure_analysis)
- `--mirror` or `-m`: Create empty mirror structure

## Output Files

### 1. Structure Report (structure_report.txt)
```
=== Application Structure Analysis ===

Directories:
  app/controllers/
  app/models/
  config/
  ...

File Types Found:
  .rb: 15 files
  .yml: 3 files
  ...

Files:
  app/controllers/application_controller.rb
  config/database.yml
  ...
```

### 2. Tree Visualization (tree_view.txt)
```
Project Structure:
├── app
│   ├── controllers
│   │   └── application_controller.rb
│   └── models
│       └── user.rb
├── config
│   └── database.yml
└── public
    └── assets
```

### 3. Mirror Structure (Optional)
Creates an empty copy of the directory structure for planning purposes.

## Ignored Items
By default, the following are ignored:
- Version control directories (.git)
- Log files (*.log)
- Temporary files (tmp/*)
- Cache directories
- System files (.DS_Store)
- Build artifacts

## Error Handling
- Directory existence validation
- Permission checking
- Clear error messaging

## Use Cases
- Project documentation
- Migration planning
- Structure analysis
- Development setup
- Backup organization
- Directory comparison

## Customization
Modify ignore patterns in the script:
```python
ignore_patterns = [
    '.git*',
    '*.log',
    'tmp*',
    # Add your patterns here
]
```

## Contributing
Contributions welcome! Feel free to:
- Submit issues
- Propose enhancements
- Create pull requests

## License
MIT