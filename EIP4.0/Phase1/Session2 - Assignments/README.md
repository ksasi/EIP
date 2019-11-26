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
     
     Epoch 00001: LearningRateScheduler reducing learning rate to 0.3.
     Epoch 1/20
     60000/60000 [==============================] - 22s 362us/sample - loss: 0.4035 - accuracy: 0.8648 - val_loss: 0.1279 - val_accuracy: 0.9627
     
     Epoch 00002: LearningRateScheduler reducing learning rate to 0.2274450341.
     Epoch 2/20
     60000/60000 [==============================] - 18s 303us/sample - loss: 0.1754 - accuracy: 0.9352 - val_loss: 0.0398 - val_accuracy: 0.9882
     
     Epoch 00003: LearningRateScheduler reducing learning rate to 0.1831501832.
     Epoch 3/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.1469 - accuracy: 0.9419 - val_loss: 0.0336 - val_accuracy: 0.9904
     
     Epoch 00004: LearningRateScheduler reducing learning rate to 0.153295861.
     Epoch 4/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.1332 - accuracy: 0.9455 - val_loss: 0.0313 - val_accuracy: 0.9917
     
     Epoch 00005: LearningRateScheduler reducing learning rate to 0.1318101933.
     Epoch 5/20
     60000/60000 [==============================] - 18s 301us/sample - loss: 0.1262 - accuracy: 0.9475 - val_loss: 0.0306 - val_accuracy: 0.9915
     
     Epoch 00006: LearningRateScheduler reducing learning rate to 0.1156069364.
     Epoch 6/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.1195 - accuracy: 0.9497 - val_loss: 0.0278 - val_accuracy: 0.9924
     
     Epoch 00007: LearningRateScheduler reducing learning rate to 0.1029512697.
     Epoch 7/20
     60000/60000 [==============================] - 18s 304us/sample - loss: 0.1118 - accuracy: 0.9525 - val_loss: 0.0284 - val_accuracy: 0.9920
     
     Epoch 00008: LearningRateScheduler reducing learning rate to 0.0927930715.
     Epoch 8/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.1148 - accuracy: 0.9504 - val_loss: 0.0237 - val_accuracy: 0.9936
     
     Epoch 00009: LearningRateScheduler reducing learning rate to 0.0844594595.
     Epoch 9/20
     60000/60000 [==============================] - 18s 301us/sample - loss: 0.1077 - accuracy: 0.9527 - val_loss: 0.0235 - val_accuracy: 0.9932
     
     Epoch 00010: LearningRateScheduler reducing learning rate to 0.0774993542.
     Epoch 10/20
     60000/60000 [==============================] - 18s 303us/sample - loss: 0.1111 - accuracy: 0.9512 - val_loss: 0.0240 - val_accuracy: 0.9931
     
     Epoch 00011: LearningRateScheduler reducing learning rate to 0.0715990453.
     Epoch 11/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.1024 - accuracy: 0.9539 - val_loss: 0.0234 - val_accuracy: 0.9932
     
     Epoch 00012: LearningRateScheduler reducing learning rate to 0.0665335995.
     Epoch 12/20
     60000/60000 [==============================] - 18s 303us/sample - loss: 0.1069 - accuracy: 0.9528 - val_loss: 0.0247 - val_accuracy: 0.9927
     
     Epoch 00013: LearningRateScheduler reducing learning rate to 0.0621375311.
     Epoch 13/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.1034 - accuracy: 0.9544 - val_loss: 0.0230 - val_accuracy: 0.9939
     
     Epoch 00014: LearningRateScheduler reducing learning rate to 0.0582863804.
     Epoch 14/20
     60000/60000 [==============================] - 18s 306us/sample - loss: 0.1016 - accuracy: 0.9536 - val_loss: 0.0235 - val_accuracy: 0.9936
     
     Epoch 00015: LearningRateScheduler reducing learning rate to 0.054884742.
     Epoch 15/20
     60000/60000 [==============================] - 18s 301us/sample - loss: 0.0995 - accuracy: 0.9540 - val_loss: 0.0215 - val_accuracy: 0.9940
     
     Epoch 00016: LearningRateScheduler reducing learning rate to 0.0518582541.
     Epoch 16/20
     60000/60000 [==============================] - 18s 303us/sample - loss: 0.0998 - accuracy: 0.9543 - val_loss: 0.0217 - val_accuracy: 0.9942
     
     Epoch 00017: LearningRateScheduler reducing learning rate to 0.0491480996.
     Epoch 17/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.1003 - accuracy: 0.9524 - val_loss: 0.0209 - val_accuracy: 0.9942
     
     Epoch 00018: LearningRateScheduler reducing learning rate to 0.0467071462.
     Epoch 18/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.0989 - accuracy: 0.9546 - val_loss: 0.0218 - val_accuracy: 0.9944
     
     Epoch 00019: LearningRateScheduler reducing learning rate to 0.0444971818.
     Epoch 19/20
     60000/60000 [==============================] - 18s 302us/sample - loss: 0.0945 - accuracy: 0.9563 - val_loss: 0.0218 - val_accuracy: 0.9938
     
     Epoch 00020: LearningRateScheduler reducing learning rate to 0.0424868999.
     Epoch 20/20
     60000/60000 [==============================] - 18s 299us/sample - loss: 0.0978 - accuracy: 0.9552 - val_loss: 0.0208 - val_accuracy: 0.9943
     <tensorflow.python.keras.callbacks.History at 0x7f8ff4e34940>
     ```
 - - Result of model.evaluate is 99.43%
 - - Strategy taken is , initially ensure the total parameters were less than 15K by reducing the filters. Ensure 1x1 is used to reduce channels i.e. as bottleneck layer. Remove batchnormalization layer before flatten layer . Then change batch size and learning rate to ensure that target accuracy of more than 99.4% reaches within 20 epochs