## DevOps Knowledge Base

This page will host all the questions and their resolutions that were addressed for the course.

## Resolved Issues
```markdown
Master branch protection ? 
It depends on the organization for smaller companies the master branch will not be protected but for larger organizations with multiple release branches it will be controlled by build teams who might lock the branch and release it as necessary.
```

```markdown
~/.m2 repository already existed ? 
Not entirely sure why you want to do this since it is just a repo, but you can provide a separate maven repository but that will be a global change.

1) Navigate to Maven Home: eg../usr/local/maven/conf 
2) Update the settings.xml where there is definition for local repository.

Note that the above change is global and you can change it back as you need. Typically you can make a copy of the settings.xml as original and provide a new version with the required override path.

.m2/repository is a local copy for all the dependencies that projects depend on, so things just get added to the repository and are never deleted. Even if you delete the repository folder if the projects are defined correctly when you do a build it will download all the dependencies. 

This is the sequence in which maven will resolve dependency when you do the build: maven -> local repo -> artifactory/nexus -> internet.
```

### About the Course
[DevOps Course by Nand](https://www.udemy.com/devops-with-git-jenkins-artifactory-and-elk-stack) 

