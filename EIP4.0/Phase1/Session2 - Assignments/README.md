# ![LOGO](images/EIP4-2.png)



- ### Assignment:
  
  1. Write the CODE9 file to achieve:
     1. 99.4% accuracy
     2. in 15k parameters
     3. within 20 Epochs
  2. You are not allowed to use:
     1. Fully connected layer to convert any 2D channel to 1D channel
     2. Use biases
  3. Submit your GitHub link with a ReadMe.md file
  4. In the ReadMe file:
     1. copy and paste your Logs for 20 epochs
     2. copy and paste the result of your model.evaluate (on test data)
     3. strategy you have taken to achieve the said results
  5. Deadline is 1 hour before your next session starts. 
  
  
  
- Result:
 - - Logs:
     
      ```
      Train on 60000 samples, validate on 10000 samples
     
     Epoch 00001: LearningRateScheduler reducing learning rate to 0.003.
     Epoch 1/20
     60000/60000 [==============================] - 18s 307us/sample - loss: 0.5462 - accuracy: 0.8163 - val_loss: 0.1993 - val_accuracy: 0.9437
     
     Epoch 00002: LearningRateScheduler reducing learning rate to 0.0022744503.
     Epoch 2/20
     60000/60000 [==============================] - 15s 250us/sample - loss: 0.1759 - accuracy: 0.9351 - val_loss: 0.1033 - val_accuracy: 0.9700
     
     Epoch 00003: LearningRateScheduler reducing learning rate to 0.0018315018.
     Epoch 3/20
     60000/60000 [==============================] - 15s 250us/sample - loss: 0.1427 - accuracy: 0.9425 - val_loss: 0.0435 - val_accuracy: 0.9865
     
     Epoch 00004: LearningRateScheduler reducing learning rate to 0.0015329586.
     Epoch 4/20
     60000/60000 [==============================] - 15s 247us/sample - loss: 0.1312 - accuracy: 0.9452 - val_loss: 0.0370 - val_accuracy: 0.9899
     
     Epoch 00005: LearningRateScheduler reducing learning rate to 0.0013181019.
     Epoch 5/20
     60000/60000 [==============================] - 15s 249us/sample - loss: 0.1203 - accuracy: 0.9483 - val_loss: 0.0326 - val_accuracy: 0.9905
     
     Epoch 00006: LearningRateScheduler reducing learning rate to 0.0011560694.
     Epoch 6/20
     60000/60000 [==============================] - 15s 250us/sample - loss: 0.1150 - accuracy: 0.9487 - val_loss: 0.0305 - val_accuracy: 0.9907
     
     Epoch 00007: LearningRateScheduler reducing learning rate to 0.0010295127.
     Epoch 7/20
     60000/60000 [==============================] - 16s 260us/sample - loss: 0.1082 - accuracy: 0.9517 - val_loss: 0.0304 - val_accuracy: 0.9916
     
     Epoch 00008: LearningRateScheduler reducing learning rate to 0.0009279307.
     Epoch 8/20
     60000/60000 [==============================] - 15s 251us/sample - loss: 0.1047 - accuracy: 0.9524 - val_loss: 0.0280 - val_accuracy: 0.9911
     
     Epoch 00009: LearningRateScheduler reducing learning rate to 0.0008445946.
     Epoch 9/20
     60000/60000 [==============================] - 15s 246us/sample - loss: 0.1012 - accuracy: 0.9538 - val_loss: 0.0247 - val_accuracy: 0.9929
     
     Epoch 00010: LearningRateScheduler reducing learning rate to 0.0007749935.
     Epoch 10/20
     60000/60000 [==============================] - 14s 241us/sample - loss: 0.0994 - accuracy: 0.9544 - val_loss: 0.0276 - val_accuracy: 0.9923
     
     Epoch 00011: LearningRateScheduler reducing learning rate to 0.0007159905.
     Epoch 11/20
     60000/60000 [==============================] - 14s 241us/sample - loss: 0.0986 - accuracy: 0.9536 - val_loss: 0.0297 - val_accuracy: 0.9915
     
     Epoch 00012: LearningRateScheduler reducing learning rate to 0.000665336.
     Epoch 12/20
     60000/60000 [==============================] - 15s 244us/sample - loss: 0.0952 - accuracy: 0.9552 - val_loss: 0.0236 - val_accuracy: 0.9926
     
     Epoch 00013: LearningRateScheduler reducing learning rate to 0.0006213753.
     Epoch 13/20
     60000/60000 [==============================] - 14s 238us/sample - loss: 0.0918 - accuracy: 0.9563 - val_loss: 0.0241 - val_accuracy: 0.9933
     
     Epoch 00014: LearningRateScheduler reducing learning rate to 0.0005828638.
     Epoch 14/20
     60000/60000 [==============================] - 15s 243us/sample - loss: 0.0932 - accuracy: 0.9566 - val_loss: 0.0257 - val_accuracy: 0.9929
     
     Epoch 00015: LearningRateScheduler reducing learning rate to 0.0005488474.
     Epoch 15/20
     60000/60000 [==============================] - 14s 242us/sample - loss: 0.0931 - accuracy: 0.9558 - val_loss: 0.0216 - val_accuracy: 0.9940
     
     Epoch 00016: LearningRateScheduler reducing learning rate to 0.0005185825.
     Epoch 16/20
     60000/60000 [==============================] - 15s 248us/sample - loss: 0.0905 - accuracy: 0.9555 - val_loss: 0.0258 - val_accuracy: 0.9928
     
     Epoch 00017: LearningRateScheduler reducing learning rate to 0.000491481.
     Epoch 17/20
     60000/60000 [==============================] - 15s 249us/sample - loss: 0.0893 - accuracy: 0.9564 - val_loss: 0.0232 - val_accuracy: 0.9936
     
     Epoch 00018: LearningRateScheduler reducing learning rate to 0.0004670715.
     Epoch 18/20
     60000/60000 [==============================] - 15s 249us/sample - loss: 0.0894 - accuracy: 0.9557 - val_loss: 0.0216 - val_accuracy: 0.9937
     
     Epoch 00019: LearningRateScheduler reducing learning rate to 0.0004449718.
     Epoch 19/20
     60000/60000 [==============================] - 15s 247us/sample - loss: 0.0884 - accuracy: 0.9556 - val_loss: 0.0221 - val_accuracy: 0.9937
     
     Epoch 00020: LearningRateScheduler reducing learning rate to 0.000424869.
     Epoch 20/20
     60000/60000 [==============================] - 15s 245us/sample - loss: 0.0858 - accuracy: 0.9567 - val_loss: 0.0223 - val_accuracy: 0.9940
     <tensorflow.python.keras.callbacks.History at 0x7fc92f150cf8>
     ```
 - - Result of model.evaluate is 99.4%
 - - Strategy taken is , initially ensure the total parameters were less than 15K by reducing the filters. Remove batchnormalization layer before flatten layer . Peform training.