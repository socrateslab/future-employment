Thanks for loading Soft Skills dataset!
 
In short this is the largest resource of soft skill phrases, 
containing 830 soft skills groupped into 190 clusters.

The dataset was produced as a part of the publication: 

@article{test,

title = "Responsible team players wanted: an analysis of soft skill requirements in job advertisements",

author = "Federica Calanca and Luiza Sayfullina and Lara Minkus and Claudia Wagner and Eric Malmi",

journal = "EPJ Data Science",

doi = "10.1140/epjds/s13688-019-0190-z",

year = "2019"
}

======================================================================
1. skills_index_final

A .csv file with the list of skills and their corresponding indices
used in the matrix from Jobs_skills_matrix_final.npz. 

Includes only final list of 830 selected soft skills.

======================================================================
2. skills_clusters

A .csv file with the list of skills groupped into clusters. Each cluster
groups skills with the same meaning, but expressed using different
wording. There are 190 clusters in total. Cluster indices correspond 
to clusters in matrix from Jobs_clusters_matrix_final.npz

Candidate confidence is the confidence score of the skill according
how likely given soft skill describes a candidate.

======================================================================
3. Jobs_skills_matrix_final.npz

Bag-of-words matrix where rows correspond to job ads and columns to the 
soft skills. The matrix contains (skill present/absent in the corresponding
job description) binary values rather than counts.

The job descriptions are taken from:
https://www.kaggle.com/c/job-salary-prediction/data

If you want to load a sparse matrix using python, use:

	from scipy import sparse
	matrix_sparse = sparse.load_npz('Jobs_skills_matrix_final.npz')
	matrix_dense = matrix_sparse.todense()

======================================================================
4. Jobs_clusters_matrix_final.npz

Bag-of-words matrix where rows correspond to job ads and columns to the 
clusters. The matrix contains (cluster present/absent in the corresponding
job description) binary values rather than counts.

The job descriptions are taken from:
https://www.kaggle.com/c/job-salary-prediction/data


If you want to load a sparse matrix using python, use:

	from scipy import sparse
	matrix_sparse = sparse.load_npz('Jobs_clusters_matrix_final.npz')
	matrix_dense = matrix_sparse.todense()

======================================================================

5. extended_list_of_skills_with_confidences

We uploaded an extended list of skills that contains all initial
soft skills mined along with the estimates (confidences) of how 
probably they descibe a candidate. The confidence formula is explained
in detail in our publication. Note that only skills of length less 
than 4 contain confidence values, since for longer phrases they were not 
calculated assuming long phrases have less ambiguity. 

======================================================================

If you have any further questions, please contact
Luiza Sayfullina: sayfullina.luiza@gmail.com or Federica Calanca: fede.calanca@gmail.com
