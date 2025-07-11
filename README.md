# dna-damage-detector-cnn
Automatic comet assay image analysis using CNN and image processing


# Automatic Classification and Counting of Cells in the Comet Assay
This project develops an automatic method for the classification and counting of cells in Comet Assay images, using Digital Image Processing and Machine Learning techniques. The Comet Assay is a widely used method to study DNA damage in cells, but traditionally its evaluation is performed manually, which is time consuming and error prone. This method automates this process, achieving an accuracy of up to 97.44%.
The project is currently being used in the Cell Biology Laboratory of the Pontificia Universidad Javeriana in Cali.

## 🔍 Main features
- **Image processing**: Uses morphological reconstruction techniques (h-domains) to improve image quality and highlight comet cells.
- **Deep learning models**: Trains and compares various convolutional neural network architectures (U-Net, UNet++, DeepLabV3+, LinkNet, PAN) with ResNet50 encoder for semantic segmentation of cells.
- **Desktop application**: Graphical interface (developed with PyQt5) allowing to upload images, process them and obtain results in labeled image format and Excel file with quantitative data for each cell (area, intensity, type of DNA damage).
- **Comprehensive validation**: Automated results were compared with manual expert evaluations, demonstrating increased accuracy and reliability.

## 📈 Outstanding results
- Accuracy (IoU Score) of up to **97.44%** with UNet++ architecture and h-dome processed images (h=200).
- Significant reduction of analysis time: from 30-60 minutes (manual) to a few seconds.
- Classification of DNA damage into five categories: no damage, mild, moderate, serious and critical.
- Favorable comparison with existing tools (such as OpenComet), surpassing them in accuracy and reducing false positives/negatives.

## 💻 Technologies used
- **Programming language**: Python 3.6
- **Main libraries**:
  - PyTorch (for neural networks).
  - OpenCV (image processing)
  - NumPy, Pandas (data management)
  - scikit-image (image transformations)
  - Albumentations (data augmentation)
  - PyQt5 (graphical interface)
  - Matplotlib, Seaborn (visualization)
- **Tools**: ImageJ (image preprocessing), Git (version control).
- **ML models**: U-Net, UNet++, DeepLabV3+, LinkNet, PAN, ResNet50 (encoder).
## 🔄 Methodology
1. **Image preprocessing**:
   - Conversion to grayscale (green channel) and application of h-domain technique to highlight cells.
   - Noise and artifacts removal by thresholding and area filtering.
2. **Model training**:
   - Comparison of five neural network architectures for semantic segmentation (three classes: head, tail, bottom).
   - Data augmentation (vertical mirror) to improve generalization.
   - Validation using IoU metrics and Dice loss.
     
3. **Validation**:
   - Comparison with manual evaluations by three researchers.
   - IoU analysis between predicted masks and Ground Truth.
  
4. **Application development**:
   - CometScanner is an application designed to efficiently and accurately address the cell sorting of the Comet Assay. Its main function is to assess the DNA damage represented by each cell in an imported image, thus facilitating research in cell biology and genetics.
   
   - The fundamental purpose of CometScanner is to provide the scientific community and professionals in cell biology and genetics with an advanced and easy-to-use tool for the accurate classification and quantification of DNA damage in Comet Assay cells. The application is designed to significantly streamline and improve the image analysis process, enabling more efficient research. This will be achieved by creating an intuitive interface that allows for the import and sorting of images from the Comet Assay, automating the sorting of cells according to DNA damage, facilitating the interpretation of results through clear visual representation, customizing the storage location of results for users, and providing help resources, such as video tutorials, to ensure a smooth user experience.

## ⚙️ Installation and use
The code for this project is available on [GitHub](https://github.com/JuanesAF/dna-damage-detector-cnn). To run the application:
1. Clone the repository:
 ```bash
 git clone https://github.com/tu-usuario/tu-repositorio.git
 cd your-repository
 ```
2. Install the dependencies (using a virtual environment is recommended):
 ```bash
 pip install -r requirements.txt
 ```
3. Run the application:

Then open your preferred Python development environment.

  ```bash
 python Application.py
 ````
**Note**: You must adjust the file path of the trained model in the ``Application`` code. In addition, you need to modify the path of the "label_class_dict.csv" file inside the "model" code.

## 📁 Estructura del Repositorio

```plaintext
Directory structure:
└── juanesaf-dna-damage-detector-cnn/
    ├── README.md
    ├── Application.py
    ├── COMETS.ui
    ├── hmax.py
    ├── label_class_dict.csv
    ├── model.py
    └── requirements.txt
```
## Contributions
Contributions are welcome. If you want to improve the project, please create a fork of the repository and send your pull requests.

## Contact
- E-mail: [jeaf016@hotmail.com](mailto:jeaf016@hotmail.com)
- LinkedIn: [LinkedIn](https://www.linkedin.com/in/juanesacostaf)
---
**Keywords**: Digital Image Processing, Artificial Intelligence, Convolutional Neural Networks, Comet Assay, DNA, Semantic Segmentation, Deep Learning.CNN, AI
