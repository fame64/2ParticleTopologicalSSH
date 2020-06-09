# 2ParticleTopologicalSSH
This are the codes used in an Undergraduate Thesis on Two Particle interactions in topological models.
All the codes are written in Python, on the Jupyter Notebook, and most of them use Numba as a way to make them faster.

EXPLANATION OF THE CODES:
All of the codes, except from the AnalyticResults, work by making a direct diagonalization of some Hamiltonian. The basic structure is: Obtain the matrix expression of the Hamiltonian in a given basis, Diagonalize it and analyse the results obtained in different ways.
The file with 1pSSH works with 1 particle models, namely Tight-Binding, SSH and Rice-Mele.
The basic program for 2-particle is 2pSSHInteractingBosons, you set some parameters: The onsite potential w0, the two coupling constants J1 J2, the hubbard repulsion coefficient U, the length of the chain N and the weight of the perturbation on w0. With this we can obtain eigenstates, energy plots and PR plots.
The 2pSSHSweepU program runs over a range of U values, and its main result is a plot of the evolution of the energies as a function of U with PR(i.e. how localized is an state) in the colorscale. It also puts figures on the most localized states. In this program Numba enhances its speed a lot.
The 2pSSHSweepN program runs changing N. Its main result is a plot of the Participation Ratio of some states as a function of N. This gives the scaling of PR which gives a lot of information of the states. In this program Numba has been used but it is pretty slow because it couldn't be parallelised as efficiently as 2pSSHSweepU.
The 2pBHMAnalyticalResults program finds a solution numerically to the bethe equations for the Bose Hubbard model. Its main result is the dispersion relation E(K) plot, it can also obtain plots E vs Index to compare to the ones that the other codes obtain.
The 2pSSHAnalyticalResults just plot the energy bands obtained for the 2pSSH model in the L infty limit, it also gives 3D plots of the bands.

WHAT TO DO IF GITHUB DOESN'T SHOW JUPYTER FILES:
Copy your github link of ‘.ipynb’ file and open this link https://nbviewer.jupyter.org on your browser. after that paste that previous link in the box ,which will be shown on the nbviewer website page and press Enter
Open google colab by using this link https://colab.research.google.com/notebooks/gpu.ipynb in the browser. after that go the ‘File’ option at the ‘top-right’ . click on this and click again on open notebook . After that go to fourth option in the header ‘GITHUB’ and paste the link in the search box and press enter. You will be able to see Your Github ‘.ipynb’ file .

DISCLAIMER:This codes aren't in any way thought or designed to be efficient nor pretty. I am not a programmer, I've just taken two undergrad level programming courses for physicists and none of them was on python. So I know there will be a lot of wrong and ugly things on the codes, the thing is that I think they work more or less for the purpose of the work.
