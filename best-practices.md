# About

This document outlines general best practices we recommend for setting up and managing your repository. This is only intended to provide a starting point for researchers that do not already have their own established methods. Feel free to deviate, but we strongly encourage keeping using good documentation and organization practices.  

# Readme Structure

This section provides a general outline for what to include in the ReadMe of your repository.

<pre>
Contact Information
- Name
- Institution
- Email
- Personal GitHub

Project Description
A brief description of the purpose of the project. 

Data
Describe where the data came from, collection methods, etc. 
This is also a good place to include links to data dictionaries. 

Computing Environmnet
Define any software/package versions used in your analysis. Alternatively, link to a dedicated file. 

File Structure
A brief overview of the structure of the repository and description of any naming conventions used.
</pre>

## Metadata About Software Environment

The ReadMe is a good place to include information about the computing environment that you’re working in. Alternatively, link to a dedicated file.  This may include programming language, version type, and package versions. If using a package manager such as Anaconda, this information can be exported to a .yml file that can be directly used alongside your work. This practice ensures that others can run your code on their machine. 

An example of this may be: 

<pre>
name: example-env
channels:
- conda-forge

dependencies:
- python=3.10
- pandas=1.5.3
- numpy=1.24.1
- matplotlib=3.7.2
- geopandas=0.13.0
- scipy=1.11.0
- jupyterlab=4.0.0
</pre>

# Repository Structure

A major goal of this organization is to make research occurring at NRS sites as transparent as possible. Towards this goal, we encourage researchers to structure their repositories in a way that makes it not only clear to an outside observer, but also easier to revisit in the future when details have been forgotten.

We recognize that each researcher may have their own defined workflows, and therefore the following is only to provide a suggestion of how to organize your work in a easy to navigate manor. An simple example file structure for a project may be: 

<pre>
earth_analysis  
|  
|--data  
|    |__01_raw  
|    |__02_clean  
|    |__03_processed  
|  
|--notebooks  
|    |__01_qc   
|    |__02_exploratory  
|    |__03_analysis  
|  
|--scripts  
|  
|--references  
|
|--outputs  
|    |__figures  
|    |__reports  
</pre>

Where "notebooks" refers to Jupyter Notebooks. Depending on the project, other useful directories may be models, pipelines, etc. Within your notebooks and scripts, it’s recommended to use relative file paths.

The use of a numbering scheme helps keep items organizing by displaying them in chronological order - e.g. the “qc” notebook directory is used to prepare the data used in the “exploratory” and “analysis” notebooks. Try to avoid using too many nested directories, as it can make navigation cumbersome. 

**A note on data**: GitHub may not be the optimal place to store your data, and rejects any file over 100MB. See “Where to Store My Data?” below for more detail. 

*For more on structuring analyses to be reproducible, see the Python package [Cookie Cutter Data Science](https://cookiecutter-data-science.drivendata.org/).*

## Naming Conventions

It’s encouraged to use consistent naming convention for all of your data, notebooks, scripts, etc. Internal consistency within your own repository is more important than consistency with other repositories, the goal is to provide a logical structure. 

Note that if prefixing files with dates, using a YYYYMMDD format will keep them in chronological order. 

It’s best to avoid using spaces, as some software and operating systems struggle with them. Use - or _ instead. 

Potential attributes to include in your file naming scheme are: 

- Experiment/project name
- Site/location
- Researcher initials
- Date range
- Type of data (e.g. meteorology, phenology)
- Condition of data (e.g. raw, clean)

### Data

Use descriptive names that clearly indicate where the data belongs in the context of your project, such as:

- [site]-[type]-[condition]-[timeframe]-[researcher]
    - sci-meteorology-raw-2003-2008-pm.csv

Use ReadMes or data dictionaries to define any acronyms (sci : santa cruz island). 

### Notebooks/Scripts

Use similarly descriptive names that will help you remember the context and purpose of the analysis, such as: 

- [Number]-[site]-[analysis-type]-[researcher]
    - 01-sci-pozo-eda-pm.ipynb

If it makes sense, use a numbering scheme to help keep track of the order of the scripts.

# Licenses

**Why do I need to choose a license for my repository?**

When hosting your work on GitHub, a license should be chosen to foster collaboration, transparency, and reproducibility. Not having a license implies that others have no right to use, modify, or distribute the code which may deter potential collaborators.

**What license should I choose?**

Commonly used licenses for researchers include the MIT license, and the three clause BSD license (BSD-3). Each of these licenses are simple and highly permissive. They both grant permission for others to use the work so long as they attribute the original author. The BSD-3 has come subtle differences, but the main one is it includes a no endorsement clause that prevents the use of the names of the original author or its contributors to promote derived products without written permission.

If your goal is open science, then the MIT license is the simplest choice. Additionally, you can initially choose a more restrictive license and then change it after publication.

For more information on licenses see [A Quick Guide to Software Licensing for the Scientist-Programmer](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002598) by Morin et al. (2012).

For additional help choosing a license, see [Choose a License](https://choosealicense.com/).

**How do I create a license?**

GitHub provides license templates that are easy to add to your repository. See GitHub’s docs [Adding a License to a Repository](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-license-to-a-repository).

# Data Management

Hosting documentation of your data management plan on GitHub is a good way to stay organized and transparent. This can either be described in the repository ReadMe, or as a separate file. If stored as a separate file, it’s a good idea to add a link to it in the ReadMe. 

## Data Management Plan

*Return to this.*

## Where to Store Data?

*Return to this.*

### Scripts to Download External Data

*Return to this.* 

# Tools for Jupyter Notebooks

Working with Jupyter Notebooks? There are tools to make life easier when collaborating with others and trying to manage version control - see [nbdime](https://nbdime.readthedocs.io/en/latest/).
