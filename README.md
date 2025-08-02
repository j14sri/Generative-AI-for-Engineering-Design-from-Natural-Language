# Text-to-Mechanism: Generative AI for Engineering Design from Natural Language

Welcome to **Text-to-Mechanism**, an innovative generative AI tool that translates plain-language engineering requirements into rough mechanical linkage diagrams or 3D mechanism concept models.

---
## Project Overview

**Text-to-Mechanism** empowers engineers, designers, and students to ideate mechanical systems by simply describing the desired motion or function in natural language. The tool leverages state-of-the-art NLP and generative deep learning to propose linkage concepts, mechanism sketches, or motion diagrams—helping automate the earliest stages of design.

- **Input:** English requirement (e.g., "I need a mechanism that converts continuous rotary motion into an oscillating movement for a pump lever.")
- **Output:** Schematic diagram, JSON of linkage data, or a 3D preview (e.g., simple SVG or interactive matplotlib plot).

---
## Key Features

- **NLP Requirement Parsing:** Understands and parses plain English into engineering constraints (motion types, degrees of freedom, desired paths).
- **Generative Model:** Uses a fine-tuned transformer or VAE to map requirements to kinematic linkage templates.
- **Concept Visualization:** Outputs diagrams using `matplotlib`, `networkx`, and simple graphical formats—rendered in-browser or as downloadable images.
- **Editable Suggestions:** Design candidates can be tweaked or re-generated for iterative refinement.
- **Export Options:** Save designs as JSON (nodes, links), SVG, or even STL for further CAD work.

---
## Tech Stack

- **Python 3.9+**
- **PyTorch** – generative neural mechanism designer
- **Transformers (HuggingFace)** – NLP model for requirement parsing
- **NetworkX / matplotlib** – for schematic mechanism drawing
- **Streamlit or Gradio** – simple interactive web interface
- **Optionally:** OpenAI API (for advanced NLP), `trimesh` for 3D mesh outputs

---
## 💡 Example Usage

### 1. Describe Your Mechanism
- "I want a mechanism that converts rotary input from a handle into a straight-line output, with a compact footprint."
  
### 2. AI Interprets & Generates

- Parses as: "Rotary to linear conversion."
- Proposes: "Slider-crank mechanism, compact orientation, 3 links."

### 3. View & Edit

- Presents a 2D linkage diagram and JSON link-data.
- Option to regenerate or adjust constraints.

---


## How It Works
### Text-to-Mechanism translates natural language engineering requirements into conceptual mechanical designs through the following pipeline:
### 1. Input Parsing via NLP
- The user inputs a plain English description of the desired mechanism or motion, for example:
   - "I want a mechanism that converts rotary input into a linear sliding output."
   -  This text is processed by an advanced Natural Language Processing (NLP) model—such as a HuggingFace transformer—that extracts key engineering intents, constraints, and motion types.
### 2. Generative Design Model
- Using a generative neural network (e.g., a Variational Autoencoder or transformer fine-tuned on mechanism datasets), the system maps these parsed requirements to feasible linkage designs. The output is structured as linkage nodes, joints, and connection types representing valid kinematic mechanisms (for example, slider-crank or four-bar linkages).
### 3. Mechanism Synthesis & Visualization
- The generated data is converted into a schematic 2D diagram using Python visualization tools like NetworkX and matplotlib, clearly illustrating link connections and motions for user review.
### 4. Interactive Refinement
- Users can adjust input constraints or regenerate alternative designs from the tool’s interactive interface, enabling rapid iterative concept development without manual drafting.
### 5. Export and Further Use
- Finalized designs can be exported as JSON files (encoding linkage data), SVG images, or simple 3D mesh formats (e.g., via trimesh) to facilitate further CAD modeling or prototyping.
### 6.Feedback & Model Improvement 
- The system can learn from user feedback to improve design relevance and diversify outputs over time, iteratively enhancing the generative model.

