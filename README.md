<h1 align="center">Hi 👋, I'm Truus Apoanaba Abuosi</h1>
<h3 align="center">I am passionate about GIS automation</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=taabuosi&label=Profile%20views&color=0e75b6&style=flat" alt="taabuosi" /> </p>

- 🔭 I’m currently working on [Adv. GIS Course Final Project](https://github.com/taabuosi/taabuosi.github.io.git)

- 🌱 I’m currently learning **Advanced GIS**

- 📫 How to reach me **taabuosi@memphis.edu**

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://linkedin.com/in/truus apoanaba abuosi" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="truus apoanaba abuosi" height="30" width="40" /></a>
<a href="https://www.youtube.com/c/truly truus" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/youtube.svg" alt="truly truus" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://www.adobe.com/in/products/illustrator.html" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/adobe_illustrator/adobe_illustrator-icon.svg" alt="illustrator" width="40" height="40"/> </a> <a href="https://www.photoshop.com/en" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg" alt="photoshop" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>

# Customizable Map Layouts Project

Welcome to the **Customizable Map Layouts** project! This repository contains a Python script that generates customizable map layouts using **GeoPandas** and **Matplotlib**. The script allows users to create professional-looking maps with several customizable elements, such as titles, legends, scale bars, and more.

## Features

- **Customizable map layouts**: Easily add or remove elements such as map title, legend, scale bar, and more.
- **Clean, professional designs**: Suitable for creating publication-quality maps.
- **Easy-to-use Python script**: Modify map elements using simple Python function calls.
- **Flexible design options**: Customizable options for each map element.

## Technologies Used

- **GeoPandas**: A Python library for working with geospatial data.
- **Matplotlib**: A plotting library to create the map layout.
- **Python**: The scripting language used for automation.

## How to Use

### 1. Clone the Repository

First, clone the repository to your local machine:

```bash
git clone https://github.com/taabuosi/taabuosi.github.io.git
cd taabuosi.github.io

pip install geopandas matplotlib
import geopandas as gpd
import matplotlib.pyplot as plt

# Function to create a customizable map layout
def create_map_layout(dataframe, title=None, legend=False, scale_bar=False):
    fig, ax = plt.subplots(figsize=(8, 6))

    # Plot the map data
    dataframe.plot(ax=ax, cmap='viridis')

    # Add map elements based on user input
    if title:
        add_title(ax, title)
    if legend:
        add_legend(ax, dataframe['column_for_legend'])  # Replace with your legend column
    if scale_bar:
        add_scale_bar(ax, "1:50000")  # Example scale bar

    plt.show()

# Add Title
def add_title(ax, title):
    ax.set_title(title, fontsize=14, fontweight='bold')

# Add Legend
def add_legend(ax, legend_data):
    ax.legend(legend_data, loc='lower right', fontsize=10)

# Add Scale Bar
def add_scale_bar(ax, scale_value):
    ax.annotate(f'Scale: {scale_value}', xy=(0.1, 0.1), xycoords='axes fraction', fontsize=10)

# Example usage
data = gpd.read_file('your_shapefile.shp')  # Replace with your own shapefile path
create_map_layout(data, title="My Custom Map", legend=True, scale_bar=True)


