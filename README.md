## The problem:
  In order to assist judges in their decision-making process, it is imperative to incorporate AI technology into the field of law. However, due to the sensitive nature of this domain, placing trust in an AI model for such crucial   
  decisions can be challenging. Therefore, our aim was to develop a highly reliable model that is grounded in real data sourced from court proceedings and actual judicial rulings.

## Motivation:
  The number of cases has increased significantly compared to the number of judges:
        - India: almost 24M court cases are pending for 17K judges.
        - Brazil: over 1.6M court cases pending for department of 5 judges.
        - US: 1.3M immigration cases for 500 judges Cases can take years if not decades to be heard 
  Difficulties:
        - - The availability of well-gathered English datasets is limited.
        - We face tough competition from the top-ranked paper in the world on paper with code.
        - The text length in the  dataset is exceptionally large.
        - BERT has limitations when it comes to processing long documents.
              What Makes BERT Stand Out? (BERT has showcased exceptional performance in various natural language processing tasks).
        - The published paper lacks implementation details.

## Objective:
  The primary objective of this project is to develop a neural legal judgment prediction system using the ECHR dataset.

  Our Main Task: binary violation classification.
  Additional Tasks:
  1- case importance classification
  2- multi-label classification. 
  
  By achieving these objectives, we seek to enhance the understanding and prediction of legal judgments, enabling more informed decision-making processes.

## Proposed Solution:
  Our methodology involves adapting the BERT model to handle long documents by employing truncation approaches and pooling techniques. We train and evaluate the adapted models using appropriate loss functions and evaluation   
  metrics. We perform hyperparameter tuning and address class imbalance in the datasets. We analyze the performance of the models and compare them with existing literature. We also explore further enhancements such as 
  incorporating larger transformer architectures. Through this methodology, we aim to overcome the limitations of BERT and achieve accurate classification and analysis of legal text data.

## Dataset:
  we utilized the European Court of Human Rights (ECHR) dataset, The dataset is provided in the form of JSON files.
  The dataset is divided into three parts: 
  the training set -> 7100
  validation set   -> 1380 
  test set         -> 2998 
  However, after hyperparameter tuning, we concatenate the training and validation sets into a single set, which is then used as the training data. 
  “This is a common approach to utilize all available labelled data for training after optimizing the hyperparameters.”

## Implementation:
  We implement 7 approaches:
      1- All-Truncation approach.
      2- Head-Truncation approach.
      3- Tail-Truncation approach.
      4- Mean-Hierarchical approach.
      5- Max-Hierarchical approach.
      6- Ro-BERT (Recurrence over bert).
      7- To-BERT (Transformer over bert).

## Testing & Evaluation:
  The evaluation of various approaches for binary violation classification. The mean pooling hierarchical approach achieved the highest performance with a macro F1 score of 83.41%, followed closely by the Ro-BERT model with a   
  score of 83.32%. The max pooling hierarchical approach attained a macro F1 score of 83.28%. Our approach achieved remarkable results, surpassing the previous state-of-the-art model's macro F1 score of 82% which is at the top 
  rank in the Papers with Code repository. For more details, you can check the following link: https://paperswithcode.com/paper/neural-legal-judgment-prediction-in-english.
  
## Future Work:
  We could enhance our work by incorporating larger transformer models such as GPT or XLNet. However, it's crucial to consider the potential challenges in terms of computational resources. These larger models typically require 
  more memory and computational power for training and inference. Therefore, it is essential to have sufficient resources or explore strategies to handle.

  these computational demands, such as distributed training or utilizing cloud-based infrastructure. Balancing the benefits of using bigger models with the practical constraints of computational resources is an important 
  consideration for further improvement in our work.




