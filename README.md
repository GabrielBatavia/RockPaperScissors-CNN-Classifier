# Rock-Paper-Scissors-Image-Classification
This Rock Paper Scissor Detector

## Notebook 
https://colab.research.google.com/drive/1tUXYwDSpNvQwfbJZ4ZAFSmL2oPG0242d?usp=sharing

## Model Architecture

The model is a Convolutional Neural Network (CNN) with the following layers:
- 4 Convolutional layers
- MaxPooling layers
- A Dense (fully connected) layer with 512 neurons
- Output layer with 3 neurons (for 3 classes: rock, paper, scissors)


The model uses the `adam` optimizer and is compiled with the categorical crossentropy loss function. 

## Training

The data is augmented using Keras's `ImageDataGenerator` to improve generalization. The model is trained for 12 epochs with early stopping to prevent overfitting.'

### Training Script
```python
history = model.fit(
    train_generator,
    epochs=15,
    validation_data=val_generator,
    callbacks=[early_stopping],
    verbose=2
)

## Result

After training, the model achieved the following performance:

- Training Accuracy: ~98.86%
- Validation Accuracy: ~97.60%

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request or open an Issue for any suggestions or improvements.
