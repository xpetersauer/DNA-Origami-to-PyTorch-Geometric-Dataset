# Convert Your DNA Origami .json Files to a PyTorch Geometric Dataset
This code takes a folder of DNA Origami Nanostructures in .json format and converts them into a Dataset format usable for Deep Learning purposes. 

# Acknowledgements
This project was my project for the Summer of 2022 in collaboration with Professor Rebecca Taylor at Carnegie Mellon University (CMU), in addition to Weitao Wang who, at the time of writing this, is a PhD Candidate at CMU. Special thanks to these individuals who had advised me while I created this projection. In addition, thanks to the members of the Microsystems and Mechanobiology Lab (MMBL) that provided me some DNA Origami nanostructures in addition to the ones I had found on Nanobase and on the websites of BIOCORD competitors.

Other sources like the .unf formatting as well as inspirations for the PyTorch dataset class design and neural network testing design are acknowledged in the .ipynb file at their respectively used spots. Nevertheless, here are direct links to these other sources of information:

- Kuťák, David, Erik Poppleton, Haichao Miao, Petr Šulc, and Ivan Barišić. 2022. "Unified Nanotechnology Format: One Way to Store Them All" Molecules 27, no. 1: 63. https://doi.org/10.3390/molecules27010063 (Github: https://github.com/barisicgroup/unf)
- Wang, Y., Wang, J., Cao, Z. et al. Molecular contrastive learning of representations via graph neural networks. Nat Mach Intell 4, 279–287 (2022). https://doi.org/10.1038/s42256-022-00447-x (Github: https://github.com/yuyangw/MolCLR)

- PyTorch Geometric Tutorials (On Node and Graph Classification): https://pytorch-geometric.readthedocs.io/en/latest/notes/colabs.html
- Stanford's Google Colab File from the class "CS224W: Machine Learning with Graphs:" https://colab.research.google.com/drive/1DIQm9rOx2mT1bZETEeVUThxcrP1RKqAn

# How to use the code:

1. Download the .ipynb file
2. Open the file and scroll down to "MAIN"
3. In a separate cell, input your the filepath to your folder of DNA Origami and input the desired task
  - Be sure to run the cells above the main file beforehand
  - if extra libraries are required on your system, you can type "!pip install [required package]" at the very top

# Sample nanostructures
This repository also includes DNA Origami Nanostructures that comply with the visualization. Feel free to use these for any other purpose

# Future Accomodations
- A Presentation to describe the project in more succinct detail
- More indications on proper use of the project

# Potential Issues
Please note that having deletions on top of crossover and "dotted horizontal connections" between strands will make the graphical representation inaccurate. If your nanostructures have these components, it's is strongly recommended for you to redesign your nanostructure such that these components are nonexistent in your design. Nevertheless, these cases are far and few in between.

# Having Issues Using the Code?
If you are having issues using the code, please feel free to contact me at "p j s a u e r AT gmail DOT com." Alternatively, feel free to describe your issue under Github Issues: https://github.com/xpetersauer/DNA-Origami-to-PyTorch-Geometric-Dataset/issues


