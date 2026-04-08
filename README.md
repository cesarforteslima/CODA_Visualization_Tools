# CODA_Visualization_Tools
New tools for Compositional Data Analysis (CoDA) to visualize ADMIXTURE results.
#
#### Script:
for K in {4..10}; do echo K${K}; python CODA_bokeh_script.py --input_file ${DB}.${K}.Q.txt --output ${DB} \
--plot_title "HGDP-1KGP WGS dataset" --pattern_file hgdp_tgp_pattern.csv --plot_height 700 --n_columns 3 \
--grid_lines --shaded_areas --centroid --save_plot svg ; done
#
# Outputs
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
