# Jira-Queries

## Useful Jira Queries

### 1. epicsOf - Query on epic links
```
issueFunction in epicsOf (Subquery)
```
Example: 
```
issueFunction in epicsOf ("resolution = unresolved")
```

### 2. issuesinEpics - Find all stories for open epics 
```
issueFunction in issuesInEpics (Subquery)
```
Example: 
```
issueFunction in issuesInEpics ("project=JRA and status = 'in progress'")
```

### 3. linkedIssuesOf - Return linked issues 
```
linkedIssuesOf(Subquery, [link name])
```
Example: 
```
linkedIssuesOf ("status="Open", "blocks") and resolution is empty
```

### 4. linkedIssuesOfRecursive - Return linked issues recursively
```
issueFunction in linkedIssuesOfRecursive (Subquery)
```
Example: 
```
issueFunction in linkedIssuesOfRecursive("issue =Jira-1")
```

### 5. linkedIssuesOfAllRecursive - Include subtask and epic links with no link type specified
```
issueFunction in linkedIssuesOf AllRecursive
```
Example: 
```
issueFunction in linkedIssues OfAllRecursive("issue =ADLEARN-711")
```

### 6. subtasksOf - Query on epic links 
```
issueFunction in subtasksOf (Subquery)
```
Example: 
```
issuefunction in subtasksOf ("issuetype = story and status != closed")
```

### 7. parentsOf - Return the parents of issues specified in the subquery 
```
issueFunction in parentsOf (Subquery)
```
Example: 
```
issueFunction in parentsOf ("resolution is empty and assignee = currentUser()")
```

### 8. expression - Compare attributes of fields
```
issueFunction in expression (Subquery, expression)
```
Example: 
```
issueFunction in expression (", "timespent > originalestimate")
```

### 9. commented - Return issues based on a comment query
```
issueFunction in expression (Subquery, expression)
```
Example: 
```
issueFunction in expression (", "timespent > originalestimate")
```
### 10. lastComment - See the last comment for an issue 
```
issueFunction in lastComment (comment query)
```
Example: 
```
issueFunction not in lastComment ("inRole Developers")
```


