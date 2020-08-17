# pooled-testing-using-hypercubes
Having read
"A strategy for finding people infected with SARS-CoV-2: optimizing pooled testing at low prevalence",
by
Leon Mutesa, Pacifique Ndishimye, Yvan Butera, Jacob Souopgui, Annette Uwineza, Robert Rutayisire, Emile Musoni, Nadine Rujeni, Thierry Nyatanyi, Edouard Ntagwabira, Muhammed Semakula, Clarisse Musanabaganwa, Daniel Nyamwasa, Maurice Ndashimye, Eva Ujeneza, Ivan Emile Mwikarago, Claude Mambo Muvunyi, Jean Baptiste Mazarati, Sabin Nsanzimana, Neil Turok, Wilfred Ndifon,
published on
medRxiv 2020.05.02.20087924; doi: https://doi.org/10.1101/2020.05.02.20087924,
I thought it might be helpful to count individuals and tests using natural numbers, and write a little piece of code to determine:
- which subsamples go into each test,
- which set of tests correspond to a given individual,
- which individual correspond to a given set of tests, 

as well as

- which number of individuals to use for each hypercube,
- the hypercube dimensions for the optimum number of individuals along each dimension, or the number of individuals along each dimension for given hypercube dimensions.
