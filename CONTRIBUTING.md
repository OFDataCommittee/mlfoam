# How to contribute to this repository

We appreciate all efforts contributing to advance data-driven modeling with OpenFOAM, may it be shared research projects, blog posts or links to software projects.

## Research projects, articles, and educational material

A general requirement for all types of listed resources is that they are **freely accessible** for everyone.

### Requirements for educational material

We consider blog posts, videos, online courses, and similar content to fall into this category. To avoid bloating the link collection, the following requirements should be fulfilled:

- the content should have a minimum length of about 1000 words (blog posts), 2min (videos), or 1h (courses); these values are not set in stone but provide only a rough orientation
- the content should be original, e.g., not an aggregation of images/animations/quotes/videos of other resources
- the content should be centered around OpenFOAM **and** data

### Requirements for software and research projects

Projects involving data-driven modeling and OpenFOAM are naturally software-heavy. Therefore, research and software projects should fulfill the following requirements:

- the project should be hosted and publicly available on a service like GitHub, Bitbucket, GitLab, etc.
- the repository should contain a README.md file providing essential information:
  - the project's scope
    - **research summary**: summary of the main results
  - installation instructions
  - usage instructions 
     - at least one tutorial case with a description (README.md) of how to use the project/software/library
  - **software**: reference to available use cases

Ideally, software-centric projects should also provide:

- Links to the respective publications (citations with DOIs)
- Design documentation that describe the architecture of the code
- Code documentation in the comments 
- A software container (Docker, Singularity) with all depenencies.
- Automatic testing
  - Build tests
  - Unit-tests
  - Automated verification and validation at least for small/simple cases.
  - All of the above packed in the CI pipeline in the project.

## Steps to contribute

If you would like to share content via this platform, please consider the following steps:

0. check the requirements listed above
1. open a new issue in this repository, provide a link to the resource, and write a one-liner describing the content; check out the available resources if you need some inspiration
2. we check the resource and add it to this repository

**Thank you for sharing your work!**
