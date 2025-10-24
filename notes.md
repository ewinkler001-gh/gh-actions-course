# Notes

# GitHub Actions consist of:
- Workflows
- Jobs
- Steps

# Workflow Events
- Repository events
- Manual Trigger: from UI, API or another workflow
- Schedule

# Workflow runners
- GitHub-hosted Standard runners
- Windows
- Ubuntu
- Mac
## Why use them GitHub-Hosted runners
 - managed service
 - VM is scoped to a job
 - always run on a clean instance

## Self-hosted runners
- Any infastructure of your choice
- Full control
- Not managed
- Can be added at repo, org or enterprise level
- Job don't necessarily run on a clean instance
- do not use in self-hosted runner in public repos

# Actions
Custom applications to perform complex, frequently reapeated tasks.
- Avoids extensive and repetitive commands
- Prevents code duplication and reduces mistakes
- configured with key-value pair
- can be combined with other steps
- can create our own actions for public or private use
- Market place has public actions

# Event Filters
- Specify which condition a specific event triggers the workflow
- Can be push to a branch, creations of a PR, etc.
- Filters can specify a specific branch, tag, path trigger a workflow
- Can also specify which ones to ignore branch_ignore, tags_ignore, paths_ignore
- branches:
-   - mian
    - 'releases/**'
  
# Activity Types
- Specify which type of certain triggers execute our workflow
- for example a pull request has types like, open, closed, synchronize, labled, assigned, edited.
- pull_request:
-   types: [opened, synchronized]
- Creates an OR condition

# Workflow Contexts
Access information about runs, variables, jobs and much more.
- GitHub provides multiple sources of data in different conexts
  ## github
    - commit SHA
    - Event name
    - Ref of branch or tag triggering workflow
  ## env
    - Contains variable that have been defined in a workflow, job or step.
    - Changes based on which part of the workflow is executing
  ## inputs
    - Contains input properties passed via the keyword with to an action, toa reusable workflow or to a manually triggered workflow.
  ## vars
    - Contains custom configuration variables set at the organization, repository and environment levels.
  ## Secrets, matrix, needs and more.

  - Look at GitHub documentation for contexts
 
  # Expressions
  - Allow us to use dynamic values
  - Can be used to reference information from multiple sources within the workflow
  - Must use the ${{ <expression> }}
  - can be any combination of literal vaues, context values, functions
  - Suppor the use of operators such as !, <,>, !+, &&, || and more
  - if: ${{ expresson }} == "value"
 
    # Variables
    - Used to set and reuse non-sensitive information
    - Single workflow - workflow level, job level, step level
    - Multiple workflows - Organization level, repository level, environment level
      - must be accesses using the vars context vars.variablename
  

