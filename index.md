---
title: Contoso Chat E2E with Azure AI Studio
permalink: index.html
layout: home
---

# Build Contoso Chat End-to-End

This repository contains the lessons and labs for a structured workshop to build Contoso Chat (a custom copilot application)  end-to-end using Azure AI Studio and Prompt flow. 


## Pre-Requisites

The following are **required** for this workshop:

1. A GitHub account - [Create a free account](https://github.com/signup)
1. An Azure subscription - [Create a free account](https://azure.microsoft.com/free/) 
1. Access to Azure Open AI service - [Request access here](https://aka.ms/oaiapply)

Familiarity with the following is **desirable**: 
1. Microsoft Azure Fundamentals - [Refresh your knowledge](https://learn.microsoft.com/en-us/training/courses/az-900t00#course-syllabus)
1. Microsoft Azure AI Fundamentals -  [Refresh your knowledge](https://learn.microsoft.com/training/paths/get-started-with-artificial-intelligence-on-azure)
1. Microsoft Azure AI Studio (preview) - [Refresh your knowledge](https://learn.microsoft.com/training/paths/create-custom-copilots-ai-studio/)
1. Using Python & Jupyter Notebooks - [Refresh your knowledge](https://learn.microsoft.com/training/paths/beginner-python/)

## Lessons

{% assign lessons = site.pages | where_exp:"page", "page.url contains '/Instructions/Lessons'" %}
| Module | Lesson |
| --- | --- | 
{% for activity in lessons  %}| {{ activity.lesson.link }} | [{{ activity.lesson.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## Labs

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| Module | Lab |
| --- | --- | 
{% for activity in labs  %}| {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
