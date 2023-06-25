
# Detecting Multidimensional Political Incivility on Social Media
This repository includes the resources associated with the paper entitled "Detecting Multidimensional Political Incivility on Social Media," authored by Sagi Pendzel, Nir Lotan, Alon Zoizner, and Einat Minkov.

> __Abstract:__
> The rise of social media has been argued to intensify uncivil and hostile online discourse. To date, there is a lack of clarity on what incivility means in the political sphere, where this limits our understanding of how common political incivility is, and which users are likely to disseminate vulgar and intolerant language. In our work, we utilize a multidimensional perspective of political incivility, developed in the fields of political science and communication, that differentiates between impoliteness and political intolerance. We present state-of-the-art incivility detection results using a large dataset of 13K political tweets, collected and annotated per this distinction. Applying political incivility detection at large-scale, we observe that political incivility demonstrates a highly skewed distribution over users. Finally, we propose an approach for modeling social context information about the tweet author alongside the tweet content, showing that this leads to improved performance on the task of political incivility detection. This latter result holds promise for socially-informed text processing in general.

An overview of the materials within the repository:

* The file `data/multilabel_incivility_dataset.csv` includes a collection of tweet IDs and their corresponding label used for training and evaluation in the context of multilabel classification (Impoliteness and Intolerance).
* The file `data/binary_incivility_dataset.csv` includes all tweet IDs labeled with binary classifications (civil/uncivil). It is important to note that this dataset contains more tweets compared to the multilabel dataset due to higher annotator agreement.
*	Within the `incivility_model_predictions.ipynb` notebook, you will find the code necessary to load the incivility classifier employed in the research paper. This code can help to produce prediction scores for new text inputs.
*	`incivility_finetuned_roberta.pt` is the fine-tuned roberta model used in the research.

**_NOTE:_**  Due to the Twitter Terms of Service, we are unable to share the full dataset here. If you are interested in obtaining the full dataset, please contact us at sagipend@gmail.com. We will be happy to assist you further.


# Usage
The code offered in this repository enables to adapt our multilabel incivility classifier to new English texts, without the necessity of retraining the classifier.

To begin, please load and run the notebook.</br>
For computing the probability of a single tweet being categorized as impolite or intolerant (or both), according to the definition employed in our paper, follow the basic usage instructions:

```python
tweet = "You are such a loser! You'll regret everything you've done to me!"

make_prediction(tweet) # [Impoliteness, Intolerance]
```
```python
>> array([0.9795, 0.0884], dtype=float32)  
```
