# ![LOGO](images/EIP4-2.png)



- ### Assignment:
  
  1. Run [this (Links to an external site.)](https://colab.research.google.com/drive/1STOg33u7haqSptyjUL40FZIxNW4XdBQK) network (base network) for 50 epochs, report Validation Accuracy **after** 50 epochs. 
  2. Add new cells at the bottom of the code, and write your own network such that:
     1. it uses depthwise separable convolution **ONLY** (no Conv2D)
     2. it uses BatchNormalization 
     3. has less than 100,000 parameters
     4. it uses proper dropout values
     5. you've mentioned the output size for each layer
     6. you've mentioned the receptive field for each layer
     7. runs for 50 epochs
     8. beats the validation score within 50 epochs (at any epoch run, doesn't need to be final one)
  3. Submit the github link 
  4. Your github links must have:
     1. 1. Assignment 3.ipynb file with your code as well as logs for both the models
        2. ReadMe.md which should have:
           1. Final Validation accuracy for Base Network
           2. Your model definition (model.add... ) with output channel size and receptive field
           3. Your 50 epoch logs
  
  
  
- Result:

- Final Validation accuracy of Base Network : 82.78 . Also best validation score is 82.82 at Epoch 43

 - - Model Definition:
     
      ```
     # Define the model
     model = Sequential()
     
     model.add(SeparableConv2D(filters = 48, kernel_size = (3, 3), padding = 'same', input_shape=(32, 32, 3), use_bias = False)) # Receptive field 3x3, Output Channel Size 32x32
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(SeparableConv2D(filters = 96, kernel_size = (3, 3), padding = 'same', use_bias = False)) # Receptive field 5x5, Output Channel Size 32x32
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(SeparableConv2D(filters = 192, kernel_size = (3, 3), padding = 'same', use_bias = False)) # Receptive field 7x7, Output Channel Size 32x32
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(SeparableConv2D(filters = 32, kernel_size = (1, 1), padding = 'same', use_bias = False)) # Receptive field 7x7, Output Channel Size  32x32
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(MaxPool2D(pool_size=(2, 2))) # Receptive field 8x8, Output Channel Size  16x16
     model.add(Dropout(0.1))
     
     model.add(SeparableConv2D(filters = 48, kernel_size = (3, 3), padding = 'same', use_bias = False)) # Receptive field 12x12, Output Channel Size  16x16
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(SeparableConv2D(filters = 96, kernel_size = (3, 3), padding = 'same', use_bias = False)) # Receptive field 16x16, Output Channel Size  16x16
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(SeparableConv2D(filters = 192, kernel_size = (3, 3), padding = 'same', use_bias = False)) # Receptive field 20x20, Output Channel Size  16x16
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     
     model.add(SeparableConv2D(filters = 32, kernel_size = (1, 1), padding = 'same', use_bias = False))  # Receptive field 20x20, Output Channel Size  16x16
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(MaxPool2D(pool_size=(2, 2)))  # Receptive field 22x22, Output Channel Size  8x8
     model.add(Dropout(0.1))
     
     
     model.add(SeparableConv2D(filters = 48, kernel_size = (3, 3), padding = 'same', use_bias = False)) # Receptive field 30x30, Output Channel Size  8x8
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(SeparableConv2D(filters = 96, kernel_size = (3, 3), padding = 'same', use_bias = False)) # Receptive field 38x38, Output Channel Size  8x8
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(SeparableConv2D(filters = 192, kernel_size = (3, 3), padding = 'same', use_bias = False)) # Receptive field 46x46, Output Channel Size  8x8
     model.add(Activation('relu'))
     model.add(BatchNormalization())
     
     model.add(MaxPool2D(pool_size=(2, 2))) # Receptive field 50x50, Output Channel Size  4x4
     model.add(Dropout(0.1))
     
     model.add(SeparableConv2D(filters = 10, kernel_size = (1, 1), padding = 'same', use_bias = False)) # Receptive field 50x50, Output Channel Size  4x4
     
     model.add(GlobalAveragePooling2D())
     model.add(Dense(num_classes, activation='softmax'))
     # Compile the model
     model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
     ```
  
 - 
   - 50 epoch logs , best validation score is 82.85 at Epoch 28

     Epoch 1/50
     391/391 [==============================] - 60s 155ms/step - loss: 1.4292 - accuracy: 0.4694 - val_loss: 2.7272 - val_accuracy: 0.1000
     Epoch 2/50
391/391 [==============================] - 47s 121ms/step - loss: 1.0240 - accuracy: 0.6316 - val_loss: 1.0199 - val_accuracy: 0.6311
     Epoch 3/50
     391/391 [==============================] - 47s 121ms/step - loss: 0.8724 - accuracy: 0.6884 - val_loss: 0.8880 - val_accuracy: 0.6959
     Epoch 4/50
     391/391 [==============================] - 47s 121ms/step - loss: 0.7684 - accuracy: 0.7284 - val_loss: 0.8447 - val_accuracy: 0.7129
     Epoch 5/50
     391/391 [==============================] - 47s 121ms/step - loss: 0.6979 - accuracy: 0.7539 - val_loss: 0.7828 - val_accuracy: 0.7356
     Epoch 6/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.6421 - accuracy: 0.7734 - val_loss: 0.6912 - val_accuracy: 0.7658
     Epoch 7/50
     391/391 [==============================] - 47s 121ms/step - loss: 0.5989 - accuracy: 0.7901 - val_loss: 0.7250 - val_accuracy: 0.7587
     Epoch 8/50
     391/391 [==============================] - 47s 121ms/step - loss: 0.5612 - accuracy: 0.8036 - val_loss: 0.6723 - val_accuracy: 0.7751
     Epoch 9/50
     391/391 [==============================] - 47s 121ms/step - loss: 0.5280 - accuracy: 0.8160 - val_loss: 0.6550 - val_accuracy: 0.7752
     Epoch 10/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.5026 - accuracy: 0.8244 - val_loss: 0.6579 - val_accuracy: 0.7712
     Epoch 11/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.4786 - accuracy: 0.8326 - val_loss: 0.6022 - val_accuracy: 0.7990
     Epoch 12/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.4532 - accuracy: 0.8415 - val_loss: 0.6413 - val_accuracy: 0.7865
     Epoch 13/50
     391/391 [==============================] - 47s 121ms/step - loss: 0.4422 - accuracy: 0.8441 - val_loss: 0.5989 - val_accuracy: 0.8017
     Epoch 14/50
     391/391 [==============================] - 47s 121ms/step - loss: 0.4214 - accuracy: 0.8512 - val_loss: 0.6059 - val_accuracy: 0.8008
     Epoch 15/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.3975 - accuracy: 0.8591 - val_loss: 0.6120 - val_accuracy: 0.7948
     Epoch 16/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.3872 - accuracy: 0.8619 - val_loss: 0.5919 - val_accuracy: 0.8078
     Epoch 17/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.3702 - accuracy: 0.8694 - val_loss: 0.5897 - val_accuracy: 0.8084
     Epoch 18/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.3609 - accuracy: 0.8713 - val_loss: 0.5951 - val_accuracy: 0.8136
     Epoch 19/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.3461 - accuracy: 0.8794 - val_loss: 0.5854 - val_accuracy: 0.8123
     Epoch 20/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.3365 - accuracy: 0.8791 - val_loss: 0.5884 - val_accuracy: 0.8174
     Epoch 21/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.3266 - accuracy: 0.8842 - val_loss: 0.6151 - val_accuracy: 0.8087
     Epoch 22/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.3141 - accuracy: 0.8889 - val_loss: 0.6382 - val_accuracy: 0.8021
     Epoch 23/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.3011 - accuracy: 0.8936 - val_loss: 0.6023 - val_accuracy: 0.8149
     Epoch 24/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2919 - accuracy: 0.8963 - val_loss: 0.6099 - val_accuracy: 0.8120
     Epoch 25/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2893 - accuracy: 0.8962 - val_loss: 0.6465 - val_accuracy: 0.8065
     Epoch 26/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2787 - accuracy: 0.8990 - val_loss: 0.6728 - val_accuracy: 0.8063
     Epoch 27/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2682 - accuracy: 0.9022 - val_loss: 0.6402 - val_accuracy: 0.8159
     Epoch 28/50
     391/391 [==============================] - 48s 121ms/step - loss: 0.2664 - accuracy: 0.9034 - val_loss: 0.5803 - val_accuracy: 0.8285
     Epoch 29/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2595 - accuracy: 0.9058 - val_loss: 0.6037 - val_accuracy: 0.8228
     Epoch 30/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2547 - accuracy: 0.9097 - val_loss: 0.6111 - val_accuracy: 0.8166
     Epoch 31/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2421 - accuracy: 0.9122 - val_loss: 0.6336 - val_accuracy: 0.8153
     Epoch 32/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2378 - accuracy: 0.9138 - val_loss: 0.6387 - val_accuracy: 0.8184
     Epoch 33/50
     391/391 [==============================] - 48s 122ms/step - loss: 0.2402 - accuracy: 0.9139 - val_loss: 0.6249 - val_accuracy: 0.8200
     Epoch 34/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.2252 - accuracy: 0.9169 - val_loss: 0.6271 - val_accuracy: 0.8218
     Epoch 35/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.2210 - accuracy: 0.9197 - val_loss: 0.6316 - val_accuracy: 0.8232
     Epoch 36/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.2167 - accuracy: 0.9213 - val_loss: 0.6371 - val_accuracy: 0.8206
     Epoch 37/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.2109 - accuracy: 0.9225 - val_loss: 0.6513 - val_accuracy: 0.8205
     Epoch 38/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.2060 - accuracy: 0.9249 - val_loss: 0.7082 - val_accuracy: 0.8140
     Epoch 39/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.2055 - accuracy: 0.9265 - val_loss: 0.6896 - val_accuracy: 0.8146
     Epoch 40/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.2008 - accuracy: 0.9259 - val_loss: 0.6708 - val_accuracy: 0.8114
     Epoch 41/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1964 - accuracy: 0.9289 - val_loss: 0.7132 - val_accuracy: 0.8083
     Epoch 42/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1905 - accuracy: 0.9287 - val_loss: 0.6893 - val_accuracy: 0.8229
     Epoch 43/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1863 - accuracy: 0.9313 - val_loss: 0.7069 - val_accuracy: 0.8099
     Epoch 44/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1865 - accuracy: 0.9315 - val_loss: 0.7424 - val_accuracy: 0.8070
     Epoch 45/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1816 - accuracy: 0.9333 - val_loss: 0.6733 - val_accuracy: 0.8210
     Epoch 46/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1697 - accuracy: 0.9368 - val_loss: 0.6647 - val_accuracy: 0.8220
     Epoch 47/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1764 - accuracy: 0.9355 - val_loss: 0.6780 - val_accuracy: 0.8247
     Epoch 48/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1715 - accuracy: 0.9376 - val_loss: 0.6817 - val_accuracy: 0.8181
     Epoch 49/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1725 - accuracy: 0.9373 - val_loss: 0.7085 - val_accuracy: 0.8199
     Epoch 50/50
     391/391 [==============================] - 47s 120ms/step - loss: 0.1649 - accuracy: 0.9400 - val_loss: 0.6947 - val_accuracy: 0.8189
     Model took 2377.63 seconds to train
     
     