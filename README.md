# IFCB_semisupervised

This repository has two notebooks. We are trying to compare if contrastive learning works for the plankton problem.
The first experiment is comparing contrastive learning against normal finetuning and transfer learning methods.

## Notes
- Data is downloaded only once. training a validation folders are created only with the images that we want to use in the experiment (we can choose them by year). Be careful because if we change the years and this two folders are not deteled, the executing won't be correct.
- We can chose the proportion of labeled examples to use. In both notebooks we can chose multiple proportions to run multiple experiments at the same time.
- We can configure which GPU is used for each notebook. We have two so each notebooks uses one so both notebooks can be run in pararel. This can be changed.

## Execution
We can always run the notebooks in the browser but usually they will take a long time. The best way to run them without the browser and save the results to a new notebook is:
```
nohup papermill notebook.ipynb experiments/result.ipynb &
``` 

