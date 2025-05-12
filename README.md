# SoccerNet Event Classification with Explainability

This project applies deep learning techniques to classify soccer events from the [SoccerNet-v2](https://www.soccer-net.org/) dataset using image data. We implemented and compared ResNet-50 and EfficientNet-B3 models, and explored model explainability through LIME and SHAP to interpret predictions and understand model decision-making.

## Project Goals

- Train convolutional neural networks (CNNs) to classify soccer events (e.g., goal, foul, offside).
- Filter and preprocess image data with limited-label classes for improved performance.
- Apply explainability techniques (LIME and SHAP) to analyze key visual features that drive predictions.

## Models Used

- **ResNet-50**  
- **EfficientNet-B3**

## Explainability Tools

- **LIME (Local Interpretable Model-agnostic Explanations)**  
  Highlights regions of the image that positively/negatively influenced the prediction.
- **SHAP (SHapley Additive exPlanations)**  
  Offers a model-aware, theoretically grounded view of feature importance.

## Dataset

- **Source**: [SoccerNet-v2](https://www.soccer-net.org/)  
- **Data**: Frame-level images from broadcast footage of professional soccer games.  
- **Labels**: Multi-class labels including goal, foul, offside, and more.  
- **Preprocessing**: Classes with fewer than 100 samples were removed to focus on well-represented event types.

## Results

- Both models achieved solid performance on filtered classes.
- SHAP and LIME highlighted meaningful visual regions relevant to specific soccer events.
- The project demonstrated how explainability tools can provide insights into black-box deep learning models in sports analytics.

## Example Outputs

| Model      | Explainability Tool | Visualization |
|------------|---------------------|----------------|
| ResNet-50  | SHAP                | ![SHAP Output](ShapOutput.png) |
| EfficientNet-B3 | LIME         | ![LIME Output](LimeOutput.png) |

## License 

This project was for educational and research purposes only.

## Setup Instructions

To run this project locally:

1. **Clone the repository**  
   `git clone https://github.com/YOUR_USERNAME/soccer-event-explainability.git`  
   `cd soccer-event-explainability`

2. **(Optional) Create a virtual environment**  
   `python -m venv venv`  
   `source venv/bin/activate`  (macOS/Linux)  
   `.\\venv\\Scripts\\activate`  (Windows)

3. **Install required packages**    
   `pip install torch torchvision shap lime matplotlib notebook`

4. **Run the notebook**  
   `SoccerNet_Code`

5. **Explore results**  
   Open `SoccerNet_Code.ipynb` to view model training and explainability outputs using SHAP and LIME.



