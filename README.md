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

## How to run Jupyter in a remote server
We have to install jupyter in the remote machine. Through ssh we can install Anaconda and then Jupyter even without having root rights. In order to run Jupyter:
```
nohup jupyter notebook &
```

This will launch Jupyter in the server but it will not be accesible from outside. In order to avoid setting a password and configuring the remote access, we can just map the jupyter port in the server with a port in our local machine using a ssh tunnel:

```
ssh -N -f -L 127.0.0.1:8888:127.0.0.1:8888 user@machine
```

Jupyter will be know accesible in localhost:8888

We can then, using VS Code and some extensions, open the remote notebooks and execute them in the server.