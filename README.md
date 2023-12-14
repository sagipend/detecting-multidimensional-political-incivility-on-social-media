
# Multidimensional Political Incivility on Twitter: Detection and Findings
This repository contains the resources associated with the paper 'Multidimensional Political Incivility on Twitter: Detection and Findings,' authored by Sagi Pendzel, Nir Lotan, Alon Zoizner, and Einat Minkov.

> __Abstract:__
> Hostile and uncivil political discourse online may negatively affect Democratic processes. In this work, we consider the task of political incivility detection. Unlike previous attempts, we utilize a multidimensional perspective of political incivility, differentiating between impoliteness--which is sometimes acceptable, and intolerance--which inherently violates the Democratic norms. We evaluate state-of-the-art classifiers on this task using a large dataset of 13K political tweets, which we collected and annotated by means of crowd sourcing. Our results and analyses illustrate the challenges involves in this task. In particular, we observe that intolerance is often expressed using implicit language, that requires higher-level semantic understanding. In addition, we apply political incivility detection at large-scale, exploring the distribution of uncivil content across individual users and across U.S. states. Our findings align and extend existing theories of Political Science and Communication.

* The [Full Dataset](https://huggingface.co/datasets/incivility-UOH/TwitCivility) and the [Detector Model](https://huggingface.co/incivility-UOH/multidim-incivility-detector) can be found on Hugging Face.

An overview of the materials within the repository:

*	Within the `incivility_model_predictions.ipynb` notebook, you will find the code necessary to load the incivility classifier employed in the research paper. This code can help to produce prediction scores for new text inputs.
*	`incivility_finetuned_roberta.pt` is the fine-tuned roberta model used in the research.


# Usage
If you prefer to load the model directly from this repository, the provided code enables the application of our multilabel incivility classifier to new English texts. This allows for the use of the model without requiring retraining.

To begin, please load and run the notebook.</br>
For computing the probability of a single tweet being categorized as impolite or intolerant (or both), according to the definition employed in our paper, follow the basic usage instructions:

```python
tweet = "You are such a loser! You'll regret everything you've done to me!"

make_prediction(tweet) # [Impoliteness, Intolerance]
```
```python
>> array([0.9795, 0.0884], dtype=float32)  
```
