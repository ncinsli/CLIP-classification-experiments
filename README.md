# CLIP classification experiments
This repository is also my interview task for ISP RAS Information systems department.


## Task structure
1. Use pretrained CLIP for a random image and text labels 
1. Evaluate CLIP on Imagenette dataset   
1. Choose a model trained on ImageNet, compare it with CLIP 
1. Try to improve CLIP with prompt-based approaches
2. Try to improve CLIP with linear probing

## Article

This repository is based on [Learning Transferable Visual Models From Natural Language Supervision
](https://arxiv.org/abs/2103.00020) article.

The experiments showed that prompting strategies (adding prefix "A photo of", embedding avergaing, etc.) generally make model's perfomance worse. The best perfomance was achieved with usin bare categories (so CLIP just needed to match an image to 10 labels which have the exact same content that original Imagenette dataset declares).
Fine-tuning CLIP with a linear layer showed the model could be easily improved to achieve 99.4% accuracy. Even though model does well on classifying pictures from Imagenette (86% accuracy), fine-tuning dramatically increased its metrics.

This notebook proved that multimodal embeddings of pictures are very informative and could be used to distinguish pictures from each other (without relying on texts, difference of which from the images model has been trained to predict). 
