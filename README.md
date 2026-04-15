# CODA_Visualization_Tools
New tools for Compositional Data Analysis (CoDA) to visualize ADMIXTURE results absed on the combined HGDP (Human Genome Diversity Project) + 1kGP (1000 Genomes Project Phase 3) data.
#
## Inputs
Inputs were kindly shared by Alicia Martin (Broad Institute, MIT and Harvard, USA) and Zan Koenig (Brown University).\
The combined HGDP-1KGP dataset was presented in:

***A harmonized public resource of deeply sequenced diverse human genomes***. Koenig Z, Yohannes MT, Nkambule LL, Zhao X, Goodrich JK, Kim HA, Wilson MW, Tiao G, Hao SP, Sahakian N, Chao KR, Walker MA, Lyu Y; gnomAD Project Consortium; Rehm HL, Neale BM, Talkowski ME, Daly MJ, Brand H, Karczewski KJ, Atkinson EG, Martin AR. Genome Research 2024 34(5):796-809. doi: 10.1101/gr.278378.123 (https://www.genome.org/cgi/doi/10.1101/gr.278378.123)
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
#
#### CODA Script:
DB=HGDP-1KGP; \
for K in {2..10}; do echo K${K}; \
python CODA_bokeh_script.py --input_file Inputs/${DB}.${K}.Q.txt --output CODA_Plots/${DB} \
--plot_title "HGDP-1KGP WGS dataset" --pattern_file Inputs/hgdp_tgp_pattern.csv \
--plot_height 700 --n_columns 3 --grid_lines --shaded_areas --centroid --save_plot svg ; done
#
###### Configuration
```
import argparse
parser = argparse.ArgumentParser(description='Parse some args')
parser.add_argument('-i', '--input_file', required=True, type=str, help='Input filename.')
parser.add_argument('-o', '--output', default="CODA_output", help='Output filename.')
parser.add_argument('-n', '--n_columns', default=3, type=int, help='Number of legend columns.')
parser.add_argument('-p', '--pattern_file', default=None, type=str, help='File with selected colors/shapes for each population.')
parser.add_argument('-t', '--plot_title', default= "", type=str, help='Title of the plot.')
parser.add_argument('-st', '--subtitle_text', default='default', type=str)
parser.add_argument('-fs', '--font_size', default=10, type=int, help='Font size of the legend.')
parser.add_argument('-pw', '--plot_width', default= 1600, type=int, help='Plot width.')
parser.add_argument('-ph', '--plot_height', default= 650, type=int, help='Plot_height.')
parser.add_argument('-gl', '--grid_lines', action='store_true', help="Show grid lines between the components.")
parser.add_argument('-gc', '--grid_circles', action='store_true', help="Show grid circles between the components.")
parser.add_argument('-c', '--centroid', action='store_true', help="Show centroids for each population.")
parser.add_argument('-ctype', '--centroid_type', default="circle", type=str, help="Assign Bokeh marker type for the centroid (e.g., circle).")
parser.add_argument('-a', '--shaded_areas', action='store_true', help="Show shaded areas for each population.")
parser.add_argument('-f', '--full_shaded_area', action='store_true', help="Show the full shaded area for all the populations.")
parser.add_argument('-k', '--keep_groups', action='store_true', help="Ensure group headers and populations stay in the same legend column.")
parser.add_argument('-save', '--save_plot', default=None, type=str, help="Save figure in SVG and PDF formats using Inkscape 1.0+.")
parser.add_argument('-nl', '--no_legend', action='store_true', help='Do not include the legend in the plot.')
parser.add_argument('-top', '--top_values', default= 10, type=int, help='Select the individuals with the highest values for each component.')
args = parser.parse_args()
```

#


