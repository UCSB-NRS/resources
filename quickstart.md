# Quickstart Guide

This guide is to help researchers that are new to GitHub get their repository up and running. It includes getting added to the organization, advice on how to structure a repository, transferring or linking an existing repository, advice on data storage, and additional topics to improve workflows. 

## Getting added to the organization

If a researcher is interested in hosting their repository in the organization, the first step is to become a member. Note that this isn’t necessary if you want us to simply add a link to your work to our index. To become a member, reach out to the emails listed in the organization overview with the subject line NRS GitHub. Please include the site that you’re working at and what you want the repository title to be.

## Setting up a repository

We will create an empty repository with your chosen name and then assign you as the admin of that repository so that you will have full control over it. We strongly encourage organizing your repository with a logical structure, such that those that are unfamiliar with your work are able to get a sense of what’s going on (see Repository Structure). Any number of users or collaborators may be added to a given repository with varying levels of permissions, and we can additionally set up teams if you’d like to manage a group (e.g. a lab group). 

### Syncing local directory to repository

Once the repository is created, you can either [clone](https://docs.github.com/en/get-started/using-git/about-git#github-and-the-command-line) the repository to your local machine, or you can [push](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository) a local directory to the repository. Either way, you will now have a local directory that’s synced with the remote repository and tracks any changes that are made. 

For more resources on using GitHub see the [GitHub Documentation](https://docs.github.com/en/get-started).

### Already have a repository?

No problem! We can either add a link to your repository to our Research Index page so that people can find your work, or we can fork your repository so that it appears in our list of repositories. For the latter, we can schedule an automated sync so that your repository stays up to date on our page.

For help with anything related to getting your repository going, reach out to our contact email. 

## Repository Structure

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
|    |__qc   
|    |__exploratory  
|    |__analysis  
|  
|--scripts  
|  
|--outputs  
|    |__figures  
|    |__reports  
</pre>
  
Where "notebooks" refers to Jupyter Notebooks. Depending on the project, other useful directories may be models, pipelines, etc. Within your notebooks and scripts, it’s recommended to use relative file paths. 

**A note on data**: GitHub may not be the optimal place to store your data, and rejects any file over 100MB. See “Where to Store My Data?” below for more detail. 

*For more on structuring analyses to be reproducible, see the Python package [Cookie Cutter Data Science](https://cookiecutter-data-science.drivendata.org/).*

## Privacy

Don’t want your work to be public before being published? Not a problem! After establishing the repository, you can set it to private. This means that only people that you specify will be able to see the contents. Once your results are published, you can set it to public to display it in the UCSB NRS organization repository list. 

### Licenses

*Return to this*

## Working with Jupyter Notebooks

Jupyter Notebooks present some unique challenges in a Git workflow when collaborating. Due to the internal representation of notebooks, it may be difficult to merge changes made when co-editing notebooks. This [guide](https://www.reviewnb.com/git-jupyter-notebook-ultimate-guide) provides instructions on how collaborating with notebooks in GitHub. 

## Advanced Features

Interested in using GitHub as a tool for collaboration? Are there multiple people in your lab group working on the same code? The following sections are extra information on tools in GitHub for project management and collaboration. These are not necessary for basic functionality.

### Teams

GitHub [Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams) can be used to facilitate collaboration within groups by providing communication features and allowing access permissions to be managed for multiple repositories (e.g. multiple projects within a lab group). 

### Projects

GitHub [Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects) is a project management tool that provides features for managing and assigning tasks, setting timelines, and planning out features.


