# Welcome to GitTree
This is a KISS (keep it stupid simple) approach to maintain a hierarchical representation of a biological haplogroup tree.

Haplotypes are sets of markers that are bound to a single genetic entity (such as a chromosome) that are unique inside a biological cell. An example is the human Y chromosome which is inherited from the father to the son as a complete unit. The same principle applies to the mitochondrial DNA which is passed down from the mother to her child. Haplotype trees assume a direct passing down of genetical information with random mutations that will propagate to later generations. In reality every DNA molecule suffers from recombination events with other genetic entities in the cell or with itself, however the haplogroup tree model completely ignores such events to reconstruct the biological phylogeny.

The idea behind GitTree is that biological haplogroup trees have the same hierarchical structure as folder based filesystems. All modern operating systems use a structure of nested folders that could be simply used to represent named haplogroups. One single required text file (always called .markers.txt) contains a list of genetic markers that define the node represented by the enclosing folder. A variety of optional files can be defined that might add additional information to a certain node. For example a .branches.order.txt file can contain a list of subbranch names that define the order how downstream branches will be displayed. By default only the names of the subfolders are shown in alphanumeric order(as defined by the operating system), but if .branches.order.txt is present, the contained names will be displayed before the remaining alphanumeric list. Another optional file could be .individuals.txt that contains a simple table of available samples that match exactly this genetic constellation (excluding the genetic constellation represented by the subbranches). Finally a .info.txt file can contain free form additional information that can be shown by the application that displays the tree.

Folders
- Represent named branches of the biological haplotree

Allowed Files:
- .markers.txt (required)
- .branches.order.txt (optional)
- .individuals.txt (optional)
- .info.txt (optional)

This GitTree repository starts with the current ISOGG and PhyloTree representation of the human Y chromosome and mitochondrial DNA. At any time it is possible to create a git branch of this repository that later can be merged to a new version of the tree in the master branch. This will allow multiple users to contribute to the repository expanding the tree with their own area of expertise. Collaborators that help me merge branches are welcome. Just contact me via thomas@tkrahn.com 
