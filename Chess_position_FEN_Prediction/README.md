## Problem Statement

**Chess Position FEN Prediction from Images**

### Core Problem
Develop a deep learning system that can automatically convert images of chess positions into their corresponding FEN (Forsyth-Edwards Notation) string representation.

### Key Components

1. **Input**: RGB images of chess boards in various positions
2. **Output**: FEN string that completely describes the chess position including:
   - Piece placement on all 64 squares
   - Active color (white/black to move)
   - Castling availability
   - En passant target square
   - Halfmove clock
   - Fullmove number

### Technical Challenges

1. **Computer Vision Tasks**:
   - Board detection and perspective correction
   - Square segmentation (64 individual squares)
   - Piece classification (12 piece types × 2 colors = 24 classes + empty squares)
   - Handling various board styles, piece sets, and lighting conditions

2. **Multi-task Learning**:
   - Simultaneous prediction of piece placement and game state information
   - Combining classification (pieces) with sequence prediction (FEN string)

### Solution Approach

Based on the code structure, the solution involves:

1. **Data Processing**:
   - Image preprocessing and augmentation
   - Square extraction from chess board images
   - FEN string parsing and encoding

2. **Model Architecture**:
   - CNN for visual feature extraction from individual squares
   - Multi-output model predicting both piece types and game state
   - Possibly using object detection or segmentation for board localization

3. **Evaluation**:
   - Accuracy metrics for piece classification
   - FEN string exact match accuracy
   - Move legality validation

### Applications
- Chess game digitization from photographs
- Chess tutorial and analysis tools
- Automated game recording from physical boards
- Chess AI integration with physical chess sets

This represents a challenging computer vision problem that combines object detection, classification, and structured output prediction in the domain of chess.
# Predict the chess positions in FEN format

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)]
1. clone the repo
2. pip install -r requirements.txt
3. streamlit run app.py


Input : Chess board image with pawns and its positions

Output : Forsyth–Edwards Notation (FEN)

![streamlit-app-2022-08-04-14-08-57](https://user-images.githubusercontent.com/48526315/182853281-0a6a31ac-05fd-4416-9292-da8e1cd94992.gif)

