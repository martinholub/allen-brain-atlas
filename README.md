# Allen Brain Atlas
Allen Brain Atlas is a collection of tools and datasets	made publicly available by the [Allen Institute for Brain Science](https://www.alleninstitute.org/what-we-do/brain-science/) . The collection features extensive data on both mouse and human brain. The relevance of such an inititative is siginifed by multiple publications in Nature, Science, Cell, Neuron and more. Moreover similar activitites are taking off also out of the neuroscience field ([Allen Institute for Cell Science](https://www.alleninstitute.org/what-we-do/cell-science/), [Human Cell Atlas](http://www.biorxiv.org/content/early/2017/05/08/121202)).

The motivation why we should dig into this data is that it can be used to enhance our current understanding of brain functioning, help us to form new hypothesis and assure that our time gets spend on acquiring novel insights. The getting in grips with the tools and datasets provided by the Allen Brain Institute requires initial time investment. This appears a worthwile tradeoff as more and more data will be made public in similar ways and it is therfore useful to know how to deal with it.

The great thing about data from Allen Institute is that it largely comes with great user interface that can be interacted with in your browser. For the large part, you should not need to do any coding (Yay!). The recomended approach would be to:
1. Play with the data in your browser
  * Get familiar with different datasets
  * Use Help tab thaty you will find on the website of every dataset
  * See how to filter for results that may be relevant for you
2. Read Technical white papers
  * These go more in detail on the methods of sample preparation, data acquisition and will give you better idea what infromation can you get out of the data
3. Return back to web interface
  * This time you should have much better understanding of what is available and how you can use it.
4. Only if you find out that the data accesible via web is not enough for you, you should think about using the Software Development Kit to access it via lines of code
  * This can be useful if you want to compute your own metrics
  * You may also want to create plots that are not available through the web interface
  * Usually more data was collected / more metrics were computed than what is accessible via the web interface
 

## How to install Allen SDK
Overall, the [Brain-Map website](http://brain-map.org/) provides very nice interface for exploratory browsing. It is impossible to replicate it localy and mostly this wouldn't be efficient approach anyway. On the other hand, should you need to extract or quantitatively compare specific bits of data across samples, you may need to use the Software Development Kit that interacts with stored data via API. If you find yourself in this situation, the following recipe will help you  quickly  set up an environment through which you can acces the data.

1. Download and install Miniconda with Python 2.7 from the following link: https://conda.io/miniconda.html. _(Skip if you already have Miniconda installed.)_
2. Open Anaconda Prompt and type: `conda env create -f allen-brain-atlas\ein.yml` where the last argument is relative path to the environment configuration file with respect to your current working directory (cwd). This will give a new environment with necessary setup.
3. In Anaconda Prompt type `activate ein` to activate your newly installed environment
4. In Anaconda prompt, change to directory that contains your IPython Notebooks (e.g. `cd allen-brain-atlas`) and start Jupyter by typing `jupyter notebook`.
5. Take a look at exemplary notebooks included in `allen-brain-atlas`. They serve as starting points for your own analysis. Documentation for the SDK is available [here](http://alleninstitute.github.io/AllenSDK/allensdk.html)