# PlantUCD Dataset

**Description:**
PlantUCD_dataset is a comprehensive collection of PlantUML code paired with corresponding software requirements, designed to assist in understanding and modeling software systems.

## Dataset Overview
- **Total Records:** X (Replace with the actual count of records)
- **File Format:**
  - JSON file containing all dataset records.
  - Supporting files include `.txt` (PlantUML full code), `.png` (class diagram images), and metadata.

## Structure of a Record
Each record in the dataset includes the following fields:

| Field         | Description                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| `HumanLang`   | Software requirement written in natural language.                                            |
| `PlantUML`    | Snippet of PlantUML code that fulfills the software requirement described in `HumanLang`.     |
| `Model`       | Indicates the class diagram model that the software requirement and code belong to.           |
| `Image`       | File name of the full class diagram image associated with the PlantUML code.                  |
| `FullCode`    | File name of the complete PlantUML code for the full class diagram.                           |

### Example Record
```json
{
    "HumanLang": "each bank is defined by a unique code and address",
    "PlantUML": "class Bank{ address }, class Bank{ code }",
    "Model": "C1",
    "Image": "1.png",
    "FullCode": "1.txt"
}
```

### Explanation of Fields
- **`HumanLang`:** Provides the natural language software requirement for the record.
- **`PlantUML`:** A snippet of PlantUML code that models the software requirement in `HumanLang`.
- **`Model`:** Identifies the class diagram model category for the software requirement and code.
- **`Image`:** Links to the PNG image file of the complete class diagram.
- **`FullCode`:** Links to the text file containing the full PlantUML code for the class diagram.

## Usage
This dataset is intended for use in:
- Research on software engineering and model-driven development.
- Automated generation and analysis of class diagrams.
- Understanding the correlation between software requirements and modeling tools.

## How to Access
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name/PlantUCD-dataset.git
   ```
2. Navigate to the dataset directory to explore the JSON file and associated resources.

## Contribution
Contributions to improve and expand the dataset are welcome! Please open an issue or submit a pull request with your changes.

## License
This dataset is provided under the MIT License. See the `LICENSE` file for details.
