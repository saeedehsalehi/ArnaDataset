# Arna: Stories from 1001 Persian Pages — A Versatile Benchmark Dataset for Intelligent Document Analysis
*ArnaDataset* is a unique collection of 1001 annotated Persian document images, carefully labeled into 7 semantic layout categories. Each image is paired with a detailed XML file that not only contains bounding boxes — but also, wherever applicable, the extracted textual content of the regions.

This dataset bridges a significant gap in Persian document understanding, enabling researchers and engineers to build smarter OCR, document parsing, and information extraction systems.



## 📌 Why ArnaDataset?

Compared to existing datasets, The Arna dataset can be beneficial not only for tasks such as **OCR**, **layout recognition**, or specifically for **recognizing tables**, **lists**, or **logos**, but it can also be very useful for the overall evaluation of **document analysis** systems.
Also, One of the notable features of this database is its consideration of various types of text, including **handwritten** and **printed** materials.
Additionally, this database is classified among multilingual databases, encompassing three languages: **Persian**, **Arabic**, and **English**.
The dataset also includes accurately annotated files with labeling information for the images. The ground-truth data is organized in XML files containing associated information about the embedded data and image.


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

├── 001A/                 # **A**rticles

├── 011C/                 # **C**atalogs

├── 100S/                 # **S**tories

├── 101AB/                # **A**cademic **B**ooks

├── 111TB/                # School **T**ext**B**ooks

├── 1001N/                # **N**ewspapers

│


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



## 📘 Annotation Guidelines

Full annotation principles, class definitions, and instructions are available in annotation_guidelines.pdf. Topics include:

 When to split vs. merge text blocks
 
 Table cell & row hierarchy
 
 How to handle overlapping or ambiguous elements
 
 Best practices for equation vs. text detection


## 📥 Accessing the Dataset

You can download Arna dataset from the [Here](https://drive.google.com/drive/folders/1KfXNsdtpNPAj8EsgpAFrD1zrXySyujHf?usp=sharing)

If you use this data and find it helpful, we’d appreciate if you could cite our dataset.

For any suggestions, questions, or want to contribute, feel free to contact [email](saeedeh_salehi@elec.iust.ac.ir).

## 📌 Versioning & Reproducibility

 Git-based annotation tracking
 
 Validated and reproducible pipeline
 
 All future changes will conform to v1.0 standards
