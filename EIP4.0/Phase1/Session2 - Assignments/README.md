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
      Epoch 1/20
      
      Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
      60000/60000 [==============================] - 10s 159us/step - loss: 0.5251 - acc: 0.8531 - val_loss: 0.0892 - val_acc: 0.9819
      Epoch 2/20
      
      Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
      60000/60000 [==============================] - 7s 120us/step - loss: 0.2465 - acc: 0.9281 - val_loss: 0.0547 - val_acc: 0.9885
      Epoch 3/20
      
      Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
      60000/60000 [==============================] - 7s 120us/step - loss: 0.1953 - acc: 0.9424 - val_loss: 0.0491 - val_acc: 0.9884
      Epoch 4/20
      
      Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
      60000/60000 [==============================] - 7s 120us/step - loss: 0.1690 - acc: 0.9468 - val_loss: 0.0390 - val_acc: 0.9915
      Epoch 5/20
      
      Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
      60000/60000 [==============================] - 7s 119us/step - loss: 0.1504 - acc: 0.9503 - val_loss: 0.0338 - val_acc: 0.9900
      Epoch 6/20
      
      Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
      60000/60000 [==============================] - 7s 120us/step - loss: 0.1356 - acc: 0.9516 - val_loss: 0.0265 - val_acc: 0.9932
      Epoch 7/20
      
      Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
      60000/60000 [==============================] - 8s 126us/step - loss: 0.1270 - acc: 0.9536 - val_loss: 0.0259 - val_acc: 0.9927
      Epoch 8/20
      
      Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
      60000/60000 [==============================] - 8s 129us/step - loss: 0.1193 - acc: 0.9549 - val_loss: 0.0236 - val_acc: 0.9934
      Epoch 9/20
      
      Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
      60000/60000 [==============================] - 7s 120us/step - loss: 0.1140 - acc: 0.9554 - val_loss: 0.0234 - val_acc: 0.9932
      Epoch 10/20
      
      Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
      60000/60000 [==============================] - 7s 121us/step - loss: 0.1084 - acc: 0.9571 - val_loss: 0.0254 - val_acc: 0.9924
      Epoch 11/20
      
      Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
      60000/60000 [==============================] - 7s 119us/step - loss: 0.1066 - acc: 0.9558 - val_loss: 0.0210 - val_acc: 0.9946
      Epoch 12/20
      
      Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
      60000/60000 [==============================] - 7s 120us/step - loss: 0.1007 - acc: 0.9566 - val_loss: 0.0217 - val_acc: 0.9937
      Epoch 13/20
      
      Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
      60000/60000 [==============================] - 7s 119us/step - loss: 0.1014 - acc: 0.9577 - val_loss: 0.0220 - val_acc: 0.9942
      Epoch 14/20
      
      Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
      60000/60000 [==============================] - 7s 119us/step - loss: 0.0986 - acc: 0.9582 - val_loss: 0.0210 - val_acc: 0.9940
      Epoch 15/20
      
      Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
      60000/60000 [==============================] - 7s 119us/step - loss: 0.0968 - acc: 0.9573 - val_loss: 0.0217 - val_acc: 0.9941
      Epoch 16/20
      
      Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
      60000/60000 [==============================] - 7s 119us/step - loss: 0.0945 - acc: 0.9571 - val_loss: 0.0212 - val_acc: 0.9945
      Epoch 17/20
      
      Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
      60000/60000 [==============================] - 7s 119us/step - loss: 0.0950 - acc: 0.9564 - val_loss: 0.0203 - val_acc: 0.9936
      Epoch 18/20
      
      Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
      60000/60000 [==============================] - 7s 124us/step - loss: 0.0910 - acc: 0.9592 - val_loss: 0.0200 - val_acc: 0.9943
      Epoch 19/20
      
      Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
      60000/60000 [==============================] - 8s 132us/step - loss: 0.0930 - acc: 0.9570 - val_loss: 0.0197 - val_acc: 0.9942
      Epoch 20/20
      
      Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
      60000/60000 [==============================] - 8s 126us/step - loss: 0.0896 - acc: 0.9593 - val_loss: 0.0199 - val_acc: 0.9947
      <keras.callbacks.History at 0x7f52f8ecfd68>
     ```
 - - Result of model.evaluate is 99.4%
 - - Strategy taken is , initially ensure the total parameters were less than 15K by reducing the filters. Remove batchnormalization layer before flatten layer . Peform training.