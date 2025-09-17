# Arna: A Multipurpose Dataset of One Thousand and One Documents for Persian Document Analysis

*ArnaDataset* is a unique collection of 1001 annotated Persian document images, carefully labeled into 7 semantic layout categories. Each image is paired with a detailed XML file that not only contains bounding boxes — but also, wherever applicable, the extracted textual content of the regions.

This dataset bridges a significant gap in Persian document understanding, enabling researchers and engineers to build smarter OCR, document parsing, and information extraction systems.



## 📌 Why ArnaDataset?

-  Language-specific: Built for Persian documents — including books, newspapers, articles, and more.
-  Semantic Layout Labels: Go beyond OCR. Understand the structure of a page.
-  High-Quality Annotation: Double-reviewed, rule-based, and validated.
-  Text Content Included: Not just where the text is, but what the text says.
-  Diverse Sources: 6 curated categories covering academic, narrative, commercial, and educational materials.



## 🔍 Dataset at a Glance

| Feature                 | Description                               |
|------------------------|-------------------------------------------|
|  Documents            | 1001 Persian document images (JPG)        |
|  Annotations          | XML files in Pascal VOC format            |
|  Layout Categories     | 7 semantic labels                         |
|  Text Content         | Embedded in XML for selected classes      |
|  Categories           | Articles, Catalogs, Stories, Textbooks, etc. |
|  Annotation Tool      | LabelImg |




## 🧠 Layout Classes

| Label     | Description                                              | Text Included? |
|-----------|----------------------------------------------------------|----------------|
| `Text`    | Main content: paragraphs, captions, footnotes            | ✅             |
| `Title`   | Document/section titles, headlines                       | ✅             |
| `Figure`  | Images, charts, illustrations                            | ❌             |
| `Logo`    | Brand symbols and graphical identifiers                  | ❌             |
| `List`    | Numbered/bulleted item blocks                            | ✅             |
| `Table`   | Structured data in rows and columns                      | ✅             |
| `Equation`| Mathematical or scientific notations                     | ❌             |

>  Each bounding box belongs to exactly one class, tightly surrounds its region, and follows strict consistency rules.



## 🗂️ Directory Structure

ArnaDataset/

│

├── 001A/        # **A**rticles

├── 011C/        # **C**atalogs

├── 100S/        # **S**tories

├── 101AB/       # **A**cademic **B**ooks

├── 111TB/       # School **T**ext**B**ooks

├── 1001N/       # **N**ewspapers

│

├── guideline.pdf  # Full annotation guideline (EN)


> Each image has an XML annotationToole same name.



## 🧾 Annotation Highlights

 ✅Format LabelImg + custoContent Extraction**Box Type**: Axis-aligned rectangles
 
 ✅ Content Extraction: Manually added for `Text`, `Title`, `Table`, and `List`
 
 ❌ Decorative elements (lines, watermarks) are excluded
 
 ❌ No overlapping boxes of the same class (IoU > 0.5 validation applied)



## 🔧 Quality Assurance

Every annotation went through a 2-phase manual review:

1. ✅ During the initial bounding box annotation
2. ✅ After text content insertion

We used custom validation scripts to check:

 Label validity
 
 Bounding box correctness
 
 Presence of <content> where needed
 
 No overlapping regions of the same class
 
 Empty or malformed files

> 🛡️ Goal: Maximize annotation integrity and machine-readability.




## 🌈 Visual Example

*Want to see it in action?*

Here's a sample visualization of how documents were labeled:

<img width="893" height="706" alt="ops" src="https://github.com/user-attachments/assets/2dad0027-c319-46d6-ba2f-42ebe1f795a9" />

<img width="492" height="365" alt="image" src="https://github.com/user-attachments/assets/6cc1508a-5070-45f2-99fd-2e4706547065" />



## 🧪 Potential Applications

 🧠 OCR for Persian (Optical Character Recognition)
 
 🧾 Document Layout Analysis
 
 📊 Table & List Extraction
 
 🤖 AI-powered Data Entry
 
 📚 Digitization of historical documents
 
 🧬 Multilingual NLP pipelines


## 📘 Annotation Guidelines

Full annotation principles, class definitions, and instructions are available in guideline.pdf. Topics include:

 When to split vs. merge text blocks
 
 Table cell & row hierarchy
 
 How to handle overlapping or ambiguous elements
 
 Best practices for equation vs. text detection


## 📌 Versioning & Reproducibility

 Git-based annotation tracking
 
 Validated and reproducible pipeline
 
 All future changes will conform to v1.0 standards


## 🤝 Contributing

Have suggestions, questions, or want to contribute?

Feel free to open an issue or pull request.
