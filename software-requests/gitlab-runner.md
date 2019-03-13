# GitLab-Runner ITAM Request 
https://docs.gitlab.com/runner/

## Business Rational

### Business Drivers 

- We need more modern software development tools that keep pace with industry standards.  
- We need tools that integrate with other tools that are industry standards while preventing us from vender lock-in.  
- We specifically need a tool that handles pipeline management far better than the existing tools which fail to fully meet the above stated business drivers. 

### Business Functionality Requirements 

We need a tool that can: 
- run a single 'job' from a pipeline in an isolated/standalone fully functional environment; 
- spin up a container within a single 'job' in the pipeline; 
- execute any kind of testing framework and generate reports on that; 
- integrate effectively with the source control environment being used by the development team; 
- deploy compiled solutions to multiple environments (SADE, SSC and Cloud) and report on the version and status of that deployment; 
- integrate the pipeline definition into the source code versioning; 

### Historical Background / Current Situation 

Currently we have two tools, TFS and Jenkins, that meet parts of the Business Drivers and Business Functionality Requirements but not all of them. 
These tools have been around for a very long time in ESDC and have proven to be tolerable given our outdated standards for development. 
SSC has stood up an instance of GitLab Community Edition (free under the MIT license) notably known as GCCode available for all government departments to collaborate and use. 
ESDC has started to use GCCode for many of our solutions. 
We have been able to integrate GCCode with TFS and Jenkins, but because these tools were not designed to work together, we have encountered many problems and need a suitable solution to go forward. 
With research and proof-of-concepts, GitLab-Runner (free under the MIT license) has proven its self to be far more effective than the current tools; even in their most optimized setup. 

## Alternative Products

### TFS Release Manager

#### Pros
- Integrates with TFS
- Existing in department

#### Cons
- Rebuilds for each enviornment
- Cumbersome UI with no alternative
- Managed seperate from source
- Difficult to do use for customized applications
- Lots of restrictions to managing the release (set in place by SADE)
- Non-issolated 'jobs'
- Limited default testing tools

### Jenkins / Maven

#### Pros
- Existing in department

#### Cons