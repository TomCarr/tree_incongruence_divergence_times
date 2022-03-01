# The implications of incongruence between gene tree and species tree topologies for divergence time estimation
The scripts presented here are relevent to the article: Carruthers et al. The implications of incongruence between gene tree and species tree topologies for divergence time estimation. Syst Biol.  

--- detailed instructions coming shortly ---

## Simple four taxon
#### To generate simulated data run [simlpe_four_taxon_simulation.R](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_four_taxon/simple_four_taxon_simulation.R).
**n_gene_trees:** number of gene trees to simulate.\
**locus_size:** length in base pairs of each simulated locus.\
**probs:** the probability that gene tree topologies are incongruent with the species tree topology in each simulated dataset.\

#### To analyse simulated data [run overall.Rev](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_four_taxon/analyse/overall.Rev) in RevBayes. 
This script will perform analyses of:
1) **The entire dataset** - using [simple_clock_script.Rev](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_four_taxon/analyse/simple_clock_script.Rev) to estimate _t_, [more_relaxed_script.Rev](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_four_taxon/analyse/more_relaxed_script_fixed.Rev) and [less_relaxed_script.Rev](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_four_taxon/analyse/less_relaxed_script_fixed.Rev) to estimate _r_, and [simple_branch_length_estimation.Rev](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_four_taxon/analyse/simple_branch_length_estimation.Rev) to estimate _n_.
2) **Concatenated loci with gene trees that are topologically congruent with the species tree** - using same scripts as for 1
3) **Individual loci, such that parameters can be estimated from congruent branches in gene trees** - using [simple_clock_scripts_gene_trees.Rev](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_four_taxon/analyse/simple_clock_script_gene_trees.Rev)

## Simple sixteen taxon
#### To generate simulated data run [simple_sixteen_taxon_simulation.R](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_sixteen_taxon/simple_sixteen_taxon_simulation.R)
Simulation needs to be repeated for imbalanced and imbalanced tree, and different levels of topological incongruence.\
**congruence_level:** output_file (needs to refer to whether tree is balanced, and level of incongruence)\
**tree:** species tree topology. Either [balanced_sixteen_taxon_cong.tre](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_sixteen_taxon/balanced_sixteen_cong.tre) or [unbalanced_sixteen_taxon_cong.tre] (https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_sixteen_taxon/unbalanced_sixteen_cong.tre)\
**incong_tree:** incongurent gene tree topology. Either [balanced_sixteen_one_incong.tre](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_sixteen_taxon/balanced_sixteen_one_incong.tre), [balanced_sixteen_two_incong.tre](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_sixteen_taxon/balanced_sixteen_two_incong.tre), [balanced_sixteen_three_incong.tre](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_sixteen_taxon/balanced_sixteen_three_incong.tre), [balanced_sixteen_four_incong.tre](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_sixteen_taxon/balanced_sixteen_four_incong.tre), [unbalanced_sixteen_incong.tre](https://github.com/pebgroup/tree_incongruence_divergence_times/blob/master/simple_sixteen_taxon/unbalanced_sixteen_incong.tre)\
**n_gene_trees:** number of gene trees to simulate\
**locus_size:** number of base pairs per locus\

## Multi-species coalescent sixteen taxon
Use for generating data in a multispecies coalescent framework with 16 taxon species tree, and analysing simulated data.

## Multi-species coalescent sixteen taxon
Use for generating data in a multispecies coalescent framework with 4 taxon species tree, and analysing simulated data.

## Empirical Example
Scripts for empirical example presented in the study.






