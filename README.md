# Convert Your DNA Origami .json Files to a PyTorch Geometric Dataset
This code takes a folder of DNA Origami Nanostructures in .json format and converts them into a Dataset format usable for Machine Learning purposes, particularly for various types of Graph Neural Networks (GNNs).

# Acknowledgements
This project was my project for the Summer of 2022 in collaboration with Professor Rebecca Taylor at Carnegie Mellon University (CMU), in addition to Weitao Wang who, at the time of writing this, is a PhD Candidate at CMU. Special thanks to these individuals who had advised me while I created this projection. In addition, thanks to the members of the Microsystems and Mechanobiology Lab (MMBL) that provided me some DNA Origami nanostructures in addition to the ones I had found on Nanobase and on the websites of BIOCORD competitors.

Other sources like the .unf formatting as well as inspirations for the PyTorch dataset class design and neural network testing design are acknowledged in the .ipynb file at their respectively used spots. Nevertheless, here are direct links to these other sources of information:

- Kuťák, David, Erik Poppleton, Haichao Miao, Petr Šulc, and Ivan Barišić. 2022. "Unified Nanotechnology Format: One Way to Store Them All" Molecules 27, no. 1: 63. https://doi.org/10.3390/molecules27010063 (Github: https://github.com/barisicgroup/unf)
- Wang, Y., Wang, J., Cao, Z. et al. Molecular contrastive learning of representations via graph neural networks. Nat Mach Intell 4, 279–287 (2022). https://doi.org/10.1038/s42256-022-00447-x ([Github Link](https://github.com/yuyangw/MolCLR))

- PyTorch Geometric Tutorials (On Node and Graph Classification): [Link to Website](https://pytorch-geometric.readthedocs.io/en/latest/notes/colabs.html)
- Stanford's Google Colab File from the class "CS224W: Machine Learning with Graphs:" [Link to Colab File](https://colab.research.google.com/drive/1DIQm9rOx2mT1bZETEeVUThxcrP1RKqAn) [Link to the Respective Tutorial](https://www.youtube.com/watch?v=-UjytpbqX4A)

# How to use the code:

1. Download the .ipynb file
2. Open the file and scroll down to "MAIN"
3. In a separate cell, input your the filepath to your folder of DNA Origami, the desired task, and your assigning function
  - Be sure to run the cells above the main file beforehand
  - if extra libraries are required on your system, you can type "!pip install [required package]" at the very top
  - In this context, the assigning function (assigningFn) is your custom function used to label a graph with a desired label. There are default functions provided and implemented into the code, but we suggest you to provide your own customized assigning function if you plan on using your dataset for more than just the specific tasks used for this project (node property classification and determining "real" from "fake" nanostructures)
    - Also note that "graphs" in this context are adjacency lists, not adjacency matrices. If your assignment function requires your graphs to be adjacency matrices, we suggest modifying the function "processData" and convert the outputs of the function "assembleGraphWithNodeAttributeDictionary" to adjacency matrices.
  
  
# Sample Nanostructures
This repository also includes DNA Origami Nanostructures that comply with the visualization. Feel free to use these for any other purpose

# Other Uses

- Visualizing Graphs
You can visualize the graphs you made using the made-visualizer. To visualize all the graphs, there are multiple ways to accopmlish this
1. If you want to visualize every graph used as you process each graph, simply input the command "visualize=True" into your main function.
2. Otherwise, you can call the visualization function "visualize" onto your graph via "visualize([name_for_your_dataset].get_dataset()[index of your graph])
3. Alternatively, you can use PyTorch Geometric to visualize a graph in your dataset

- Modifying Functions
This project, while it has been coded to properly work on my Mac, has not properly been properly tested on other systems. As such, modifications may be required to account for legacy code. If there are errors in your code, each processing step is organized in its cell so that this modification process is easier for you. Feel free to modify any of the functions provide (in particular, the function for processing the data as well as the classes themselves seem to be the most suspected for customization).

# Future Work
Currently, this project is complete as-is. However, there are several avenues in which it can be improved on. Mainly, incorporating all the functions into one giant class instead of requiring the user to run each individual cell would be more user-friendly. In addition, runtime is also a concern, as it takes around fifteen minutes to process 150 graph structures. Please feel free to contribute and I will give you credit on this repository.

# Potential Issues
Please note that having deletions on top of crossover and "dotted horizontal connections" between strands will make the graphical representation inaccurate. If your nanostructures have these components, it's is strongly recommended for you to redesign your nanostructure such that these components are nonexistent in your design. Nevertheless, these cases are far and few in between.

# Having Issues Using the Code?
If you are having issues using the code, please feel free to contact me at "p j s a u e r AT gmail DOT com." Alternatively, feel free to describe your issue under [Github Issues](https://github.com/xpetersauer/DNA-Origami-to-PyTorch-Geometric-Dataset/issues)


