# PlantUCD Dataset

**Description:**
PlantUCD_dataset is a comprehensive collection of PlantUML code paired with corresponding software requirements, designed for Neural Machine Translation (NMT) in automatic class diagram modeling.

## Dataset Overview
- **File Format:**
  - JSON file containing all dataset records.

## Structure of a Record
Each record in the dataset includes the following fields:

| Field              | Description                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------|
| `HumanLang`        | Software requirement written in natural language.                                             |
| `PlantUML`         | Snippet of PlantUML code that fulfills the requirement described in `HumanLang`.              |
| `Model`            | Identifier of the class diagram model the requirement belongs to.                             |
| `RequirementIndex` | Index of the requirement within the associated model.                                         |
| `Output_AST`       | JSON representation of the class diagram structure as an Abstract Syntax Tree (AST).         |

### Example Record
```json
{
  "HumanLang": "A bank is uniquely identified by its code and physical location.",
  "PlantUML": "class Bank { address }\nclass Bank { bankCode }",
  "Model": "A1",
  "RequirementIndex": "0",
  "Output_AST": {
    "type": "root",
    "children": [
      {
        "type": "class",
        "value": "Bank",
        "children": [
          {
            "type": "attribute",
            "value": "address",
            "visibility": ""
          },
          {
            "type": "attribute",
            "value": "bankCode",
            "visibility": ""
          }
        ]
      }
    ]
  }
}
```

### Explanation of Fields

- **`HumanLang`**: Natural language description of a software requirement.
- **`PlantUML`**: PlantUML code modeling the entities or relations described in `HumanLang`.
- **`Model`**: Identifier of the class diagram model (e.g., A1, B2).
- **`RequirementIndex`**: Numeric index indicating the order or position of the requirement within the model.
- **`Output_AST`**: JSON Abstract Syntax Tree representing the structure of the class diagram extracted from the PlantUML code.


## Usage
This dataset is intended for use in:
- Research on software engineering and model-driven development.
- Automated generation and analysis of class diagrams.
- Understanding the correlation between software requirements and modeling tools.

## How to Access
1. Clone the repository:
   ```bash
   git clone https://github.com/FeisalAlaswad/PlantUCD-dataset-full.git
   ```
2. Navigate to the dataset directory to explore the JSON file and associated resources.

## Contribution
Contributions to improve and expand the dataset are welcome! Please open an issue or submit a pull request with your changes.

## License
This dataset is provided under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

The authors would like to express their sincere gratitude to:

- **Department of Computing Technologies, SRM Institute of Science and Technology**  
- **Department of Computer Engineering, Aleppo University**
- **Department of Computer Engineering and Automation, Damascus University**  
- **University of Brescia**  

for their invaluable support throughout this research.

We extend our heartfelt gratitude to:  
- **Prof. Amer Bouchi**  
- **Prof. Hazem Issa**  
- **Mr. Mohammad Aljaddouh**  
- **Mrs. Fatina Alhamwi**  
- **Mr. Firas Zeineddine**  
- **Mrs. Batoul Aljaddouh**  

for their invaluable contributions.


