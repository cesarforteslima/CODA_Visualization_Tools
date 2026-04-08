# CODA_Visualization_Tools
New tools for Compositional Data Analysis (CoDA) to visualize ADMIXTURE results absed on the combined HGDP (Human Genome Diversity Project) + 1kGP (1000 Genomes Project) data.
#
#### CODA Script:
DB=HGDP-1KGP
for K in {2..10}; do echo K${K}; \
python CODA_bokeh_script.py --input_file ${DB}.${K}.Q.txt --output ${DB} \
--plot_title "HGDP-1KGP WGS dataset" --pattern_file hgdp_tgp_pattern.csv \
--plot_height 700 --n_columns 3 --grid_lines --shaded_areas --centroid --save_plot svg ; done
#
## Outputs
###### &emsp;[CODA plot for ADMIXTURE results at K=2 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K2_interactive_plot_with_centroids.html)

###### &emsp;[CODA plot for ADMIXTURE results at K=3 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K3_interactive_plot_with_centroids.html)

###### &emsp;[CODA plot for ADMIXTURE results at K=4 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K4_interactive_plot_with_areas_and_centroids.html)

###### &emsp;[CODA plot for ADMIXTURE results at K=5 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K5_interactive_plot_with_areas_and_centroids.html)

###### &emsp;[CODA plot for ADMIXTURE results at K=6 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K6_interactive_plot_with_areas_and_centroids.html)

###### &emsp;[CODA plot for ADMIXTURE results at K=7 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K7_interactive_plot_with_areas_and_centroids.html)

###### &emsp;[CODA plot for ADMIXTURE results at K=8 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K8_interactive_plot_with_areas_and_centroids.html)

###### &emsp;[CODA plot for ADMIXTURE results at K=9 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K9_interactive_plot_with_areas_and_centroids.html)

###### &emsp;[CODA plot for ADMIXTURE results at K=10 based on the HGDP-1KGP WGS dataset.](https://raw.githack.com/cesarforteslima/CODA_Visualization_Tools/main/CODA_Plots/HGDP-1KGP_K10_interactive_plot_with_areas_and_centroids.html)
#
## Inputs
Inputs were kindly shared by Alicia Martin (Broad Institute, MIT and Harvard, USA) and Zan Koenig (Brown University).
The combined HGDP-1KGP dataset was presented in:

***A harmonized public resource of deeply sequenced diverse human genomes***. Koenig Z, Yohannes MT, Nkambule LL, Zhao X, Goodrich JK, Kim HA, Wilson MW, Tiao G, Hao SP, Sahakian N, Chao KR, Walker MA, Lyu Y; gnomAD Project Consortium; Rehm HL, Neale BM, Talkowski ME, Daly MJ, Brand H, Karczewski KJ, Atkinson EG, Martin AR. Genome Research 2024 34(5):796-809. doi: 10.1101/gr.278378.123.
https://www.genome.org/cgi/doi/10.1101/gr.278378.123


