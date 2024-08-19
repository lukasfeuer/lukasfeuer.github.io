---
title: Source Control for Data Analysts
author: Lukas Feuer
date: '2022-07-15'
menu:
  sidebar:
    name: Source Control
    identifier: source_control
    weight: 100
categories: ["R"]
tags: ["R", "git", "meta programming"]
---

In this post I describe my continuing efforts to integrate some of the tools I use for most of my (work related) data analyses. The continuing challenge is to implement a solid source control and (RStudio-) project structure while still making it possible for non-technical colleagues to access resources and to contribute.

## The Workflow

Working in a corporate environment as a Data Analyst and with a team of professionals who mostly are not Data Analysts and are not familiar with source control tools like Git and Github poses some significant challenges in implementing a workflow using such tools.

-   MS Tools and Share Point

-   Data Sensitivity

A typical project structure might look like this (compare to watson)

/project_name/

R/

sql/

data/

In reality however a project might require a much more complex directory structure for different stages of the project or to organize (data) files that are used for completely different purposes. For a pure Data Analyst team it might not be a problem to adhere to a strict naming convention for files and just put all data into the data/ directory since one usually accesses the data from a R-script which provides the necessary context for understanding the context and purpose of the data.

The problem with this approach however comes when working in the aforementioned constellations. Often files follow different naming schemes (or none at all) and are manually opened and edited by colleagues who don't code. They have to manually go through the data/ folder without any helpful context except a more or less well chosen file name.

This leads to many data files grouped in many different folders (and sub-folders) with other files like presentations, saved Emails and text documents. This makes exclusion of sensitive data within the .gitignore file very difficult since there are a lot of different folders and file types to be considered that should not be uploaded.

This holds true even if a private repository on Github is used. The problem of avoiding tracking of data-files in with Git is not just a purely security based concern but also a data protection issue. If the files also include personal information, like for example names and addresses, in many cases the data must not be uploaded to Github.

This structure poses some challenges

-   Modifiing renv:: to match these requirements

------------------------------------------------------------------------

# Annotations

<p>

<ul>

<li>Lorem Ipsum</li>

<li>Lorem Ipsum</li>

<li>Lorem Ipsum</li>

</ul>

</p>

------------------------------------------------------------------------

<details>

<summary><b>Technical note</b>: Incorporating a flexdashboard into blogdown</summary>

<p>Lorem Ipsum</p>

</details>
