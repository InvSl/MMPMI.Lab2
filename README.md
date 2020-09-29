# LAB2.0

NUM_CLASSES = 6

____________________________________________________________________________________
  ## Нейросеть (1). Исходная нейросеть

  BATCH_SIZE = 32
  lr = 0.000001
   
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
      
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_categorical_accuracy%20(1).svg)
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_loss%20(1).svg)
   
  ## Нейросеть (2). Добавление полносвязного слоя 
  
  Добавляем 1 полносвязный слой (filters=8, kernel_size=3)
  
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
       
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_categorical_accuracy%20(2).svg)
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_loss%20(2).svg)
        
  ## Нейросеть (3). Увеличиваем размер сети (2)
  
   Добавляем 1 полносвязный слой (filters=8, kernel_size=3)
   
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
  
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_categorical_accuracy%20(3).svg)
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_loss%20(3).svg)
        
  ## Нейросеть (4). Увеличиваем число фильтров в свёрточных слоях сети (3) 
  
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
      
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_categorical_accuracy%20(4).svg)
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_loss%20(4).svg)
   
  ## Нейросеть (5). Сеть (4). Тест на влияние learning_rate 
  
  lr = 0.0000005 (вместо 0.000001)
  
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
      
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_categorical_accuracy%20(5).svg)
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_loss%20(5).svg)
   
  ## Нейросеть (6). Сеть (5) с измененным числом фильтров
  
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=64, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
      
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_categorical_accuracy%20(6).svg)
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_loss%20(6).svg)
  
  ## Нейросеть (7).
  
  BATCH_SIZE = 16
  lr = 0.0000001
  
        tf.keras.layers.Input(shape=(224,224,3)),
        tf.keras.layers.Conv2D(filters=8, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=16, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=32, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Conv2D(filters=64, kernel_size=3),
        tf.keras.layers.MaxPool2D(),
        tf.keras.layers.Flatten(),
        tf.keras.layers.Dense(NUM_CLASSES, activation=tf.keras.activations.softmax)
      
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_categorical_accuracy%20(7).svg)
  ![Image alt](https://raw.githubusercontent.com/InvSl/MMPMI.Lab2/c1f799a972a9c163a57f346b8acd56906385da56/tensorboard/epoch_loss%20(7).svg)
