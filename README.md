
# Detecting and Characterizing Political Incivility on Social Media
This repository includes the resources associated with the paper entitled "Detecting and Characterizing Political Incivility on Social Media," authored by Sagi Pendzel, Nir Lotan, Alon Zoizner, and Einat Minkov.

> __Abstract:__
> Researchers of political communication study the impact and perceptions of political incivility on social media. Yet, so far, relatively few works attempted to automatically detect and characterize political incivility. In our work, we study political incivility in Twitter, presenting several research contributions. First, we present state-of-the-art incivility detection results using a large dataset, which we collected and labeled via crowd sourcing. Importantly, we distinguish between uncivil political speech that is impolite and intolerant anti-democratic discourse. Applying political incivility detection at large-scale, we derive insights regarding the prevalence of this phenomenon across users, and explore the network characteristics of users who are susceptible to disseminating uncivil political content online. Finally, we propose an approach for modeling social context information about the tweet author alongside the tweet content, showing that this leads to significantly improved performance on the task of political incivility detection. This result holds promise for related tasks, such as hate speech and stance detection.

An overview of the materials within the repository:

* The file `data/multilabel_incivility_dataset.csv` includes a collection of tweet IDs and their corresponding label used for training and evaluation in the context of multilabel classification (Impoliteness and Intolerance).
* The file `data/binary_incivility_dataset.csv` includes all tweet IDs labeled with binary classifications (civil/uncivil). It is important to note that this dataset contains more tweets compared to the multilabel dataset due to higher annotator agreement.

**_NOTE:_**  Due to the Twitter Terms of Service, we are unable to share the full dataset here. If you are interested in obtaining the full dataset, please contact us at sagipend@gmail.com. We will be happy to assist you further.


