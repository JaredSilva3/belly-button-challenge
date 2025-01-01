# Belly Button Biodiversity Dashboard

## Overview of the Project

The goal of this project was to create an interactive dashboard to explore the Belly Button Biodiversity dataset. This dataset catalogs the microbes found in human navels and reveals that some microbial species (called operational taxonomic units, or OTUs) are common, while others are rare.

### What the Dashboard Does:
1. Displays the top 10 OTUs found for a selected individual.
2. Shows a bubble chart with all OTUs for a sample.
3. Displays demographic information for the selected individual.
4. Updates all charts and information when a new individual is selected.

---

## How the Dashboard Works

### Data Source
The dashboard uses a dataset stored at this URL:  
`https://static.bc-edx.com/data/dl-1-2/m14/lms/starter/samples.json`.

### Features
1. **Bar Chart**:
   - Shows the top 10 OTUs for a selected sample.
   - Uses `sample_values` for bar lengths, `otu_ids` as labels, and `otu_labels` as hover text.
   
2. **Bubble Chart**:
   - Displays all OTUs for a sample.
   - Uses `otu_ids` for the x-axis, `sample_values` for the y-axis, and `otu_labels` for hover text.
   - Marker size and color represent `sample_values` and `otu_ids`.

3. **Metadata Panel**:
   - Displays demographic information for the selected individual.
   - Updates when a new sample is selected.

4. **Dropdown Menu**:
   - Lets users select a sample ID to update all the charts and demographic info.

---

## How the Code Works

1. **`buildMetadata(sample)`**:
   - Fetches metadata for the selected sample.
   - Loops through key-value pairs to display demographic info.
   - Updates the `#sample-metadata` panel.

2. **`buildCharts(sample)`**:
   - Fetches sample data.
   - Creates a bar chart with the top 10 OTUs.
   - Creates a bubble chart with all OTUs for the sample.

3. **`init()`**:
   - Runs when the page loads.
   - Populates the dropdown menu with sample IDs.
   - Displays the data for the first sample by default.

4. **`optionChanged(newSample)`**:
   - Updates the metadata and charts when a new sample is selected from the dropdown.

---

## Results

The dashboard successfully:
- Displays the top 10 OTUs and all OTUs for a sample.
- Shows demographic info for each individual.
- Dynamically updates charts and info based on user selection.
