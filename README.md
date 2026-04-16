# PlantUCD Dataset

## Citation
If you use this work or dataset in academic research, please cite it as follows:
```bibtex
@article{PLANTUCD_2026,
  title   = {PLANTUCD: A Dataset of Software Requirements and Corresponding PlantUML-Based Class Diagrams},
  author  = {Alaswad, Feisal and Poovammal, E and Aljaddouh, Batoul},
  journal      = {TechRxiv},
  year         = {2026},
  doi          = {10.36227/techrxiv.176772833.35984408/v1},
  url          = {https://doi.org/10.36227/techrxiv.176772833.35984408/v1},
  note         = {Preprint, posted Jan 06 2026}
}

```

## 📄 Reference

If you use this dataset, please cite:

Alaswad, F., *PLANTUCD: A Dataset of Software Requirements and Corresponding PlantUML-Based Class Diagrams*, TechRxiv, 2025.  
Available at: https://www.techrxiv.org/users/1012792/articles/1372916-plantucd-a-dataset-of-software-requirements-and-corresponding-plantuml-based-class-diagrams



**Description:**
PlantUCD_dataset is a comprehensive benchmark dataset consisting of natural-language software requirements paired with corresponding PlantUML class diagram representations. The dataset is designed to support Neural Machine Translation (NMT), Large Language Models (LLMs), and sequence-to-structure learning approaches for automatic UML class diagram generation from textual requirements.

The dataset enables research in automated software modeling, requirements engineering, and AI-assisted software design by providing aligned requirement-to-diagram structural mappings.

---

## Dataset Overview

### Dataset Size

| Metric | Train Set | Test Set |
|-------|-----------|----------|
| Total Samples | 8,137 | 1,409 |
| Total Classes | 18,264 | 3,152 |
| Total Attributes | 20,896 | 3,531 |
| Total Methods | 8,894 | 1,609 |
| Total Relations | 10,208 | 1,737 |

Total dataset size: **9,546 requirement–diagram pairs**

---

### Structural Statistics per Sample

| Metric | Train Set | Test Set |
|-------|-----------|----------|
| Avg Classes / Sample | 2.24 | 2.24 |
| Avg Attributes / Sample | 2.57 | 2.51 |
| Avg Methods / Sample | 1.09 | 1.14 |
| Avg Relations / Sample | 1.25 | 1.23 |

---

### Maximum Structural Complexity per Sample

| Metric | Train Set | Test Set |
|-------|-----------|----------|
| Max Classes | 6 | 4 |
| Max Attributes | 13 | 10 |
| Max Methods | 6 | 8 |
| Max Relations | 5 | 4 |

---

### Relation Type Distribution

| Relation Type | Train Set | Test Set |
|--------------|-----------|----------|
| Association | 5,082 | 854 |
| Link | 3,780 | 593 |
| Extension | 612 | 89 |
| Composition | 552 | 93 |
| Aggregation | 128 | 72 |
| Dependency | 54 | 36 |

---

## File Format

The dataset is provided as:

- JSON format
- Each record contains:
  - natural-language software requirement description
  - corresponding PlantUML class diagram representation
  - structured diagram components (classes, attributes, methods, relations)

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









