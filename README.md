# RescuEye: Thermal Image-Based Victim Detection System

## Overview
RescuEye is an innovative disaster response system that leverages thermal imaging and machine learning to detect and classify victims in disaster areas. Traditional ML models often struggle with victim detection due to similar background-foreground colors (e.g., victims covered in debris). RescuEye overcomes this limitation by detecting victims based on body temperature through thermal imaging.

## Technologies Used
- **Python 3.8+**
- **Streamlit**: For interactive web application interface
- **OpenCV (cv2)**: For image processing and manipulation
- **Roboflow**: For ML model deployment and predictions
- **Supervision**: For annotation and visualization
- **NumPy**: For numerical computations
- **Pandas**: For data manipulation and analysis
- **PIL (Python Imaging Library)**: For image handling
- **Matplotlib**: For visualization and plotting

## Features and Results

### 1. Victim Detection
The system accurately detects victims using thermal signatures, even in conditions where traditional visual detection fails.

#### Input Image
![VictimDetectionInput](https://github.com/user-attachments/assets/59a94272-fee9-42c7-9c55-ca413e228367)


#### Output Image
<div style="display: flex; justify-content: space-between;">
    <div style="flex: 1; padding: 10px;">
        <h4>Input Image</h4>
        <img src=![DetectedVictims](https://github.com/user-attachments/assets/b4b53aee-8a61-4782-9f3b-1e643bf411f3) alt="Input Thermal Image" width="400"/>
        <p><em>Thermal image input showing disaster scene</em></p>
    </div>
    <div style="flex: 1; padding: 10px;">
        <h4>Output Image</h4>
        <img src="path_to_output_image.jpg" alt="Detected Victims" width="400"/>
        <p><em>Annotated output showing detected victims</em></p>
    </div>  
</div>

![Heatmap of Detected Victims](https://github.com/user-attachments/assets/66f56fbe-6d6f-4a89-9000-e96b43ceee98)


### 2. Resource Allocation
Based on the number of detected victims, the system calculates necessary relief materials.

#### Input 
Number of Victims Detected

#### Output Calculation
![Resource allocation-NonFoodReliefItems](https://github.com/user-attachments/assets/9ffc6e27-0446-4a1f-8b39-72e587bdfe66)
![FoodRelief Items](https://github.com/user-attachments/assets/df5b3b8e-953f-4fc9-b098-2028577f72a6)


### 3. Injury Classification
Classifies victims based on their thermal signatures to prioritize medical attention.

#### Input Thermal Image
![InjuredPerson](https://github.com/user-attachments/assets/4dbcb259-eaaa-44c1-aad2-41c1585880c1)  ![Non Injured](https://github.com/user-attachments/assets/fd960aa3-a9cd-4cc2-b566-76a68a1450d2)

#### Output Classification
![Injured](https://github.com/user-attachments/assets/f8e0c489-4ac3-48a1-a7b6-07cdb0f540c9)  ![NonInjuredResult](https://github.com/user-attachments/assets/6bfdfb3d-d306-48bc-ba66-d76354c89ebb)

## Installation

```bash
# Clone the repository
git clone [repository-url]

# Install required dependencies
pip install -r requirements.txt
```

## Required Dependencies
```text
streamlit
roboflow
supervision
opencv-python
numpy
pandas
Pillow
matplotlib
```

## Usage

### Running the Application
```bash
streamlit run app.py
```

### Application Pages
1. **Home**: System overview and introduction
2. **Detect Victims**: 
   - Upload thermal images
   - View detection results
   - Get resource allocation recommendations
3. **Injury Classification**:
   - Upload thermal images
   - View injury severity analysis
4. **Further Scope & Credits**

## Configuration Parameters
- Temperature threshold: 89.06°F (injury classification)
- Binary threshold: 185-200 (image processing)
- Minimum area: 2400 pixels (detection consideration)
- Conversion factor: 2.25 (pixel-to-temperature)

## Data Sources
- [FLIR Thermal Images Dataset](https://www.kaggle.com/datasets/deepnewbie/flir-thermal-images-dataset)
- [People Thermal Images Database](https://figshare.com/articles/dataset/Data_set_of_thermal_images_of_people_in_forested_areas_/24473002/1)
- UNHCR Food and Nutrition Needs in Emergencies

## Research Paper
For detailed methodology and findings, refer to our paper: [IJIRT164591_PAPER.pdf](https://ijirt.org/publishedpaper/IJIRT164591_PAPER.pdf)

##Datasets
[FLIR Thermal Images Dataset](https://www.kaggle.com/datasets/deepnewbie/flir-thermal-images-dataset)
[People thermal images database](https://figshare.com/articles/dataset/Data_set_of_thermal_images_of_people_in_forested_areas_/24473002/1)

##Resource Allcoation
Resource allocation in disaster areas is with reference to UNHCR Food and Nutrition Needs in Emergencies:[PDF](https://www.unhcr.org/media/food-and-nutrition-needs-emergencies)

## Sample Images
Sample images for testing are available in:
- Victim Detection: `GOOD_TO_GO` folder
- Injury Classification: `Injury_classification` folder

