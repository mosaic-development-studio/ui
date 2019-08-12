# JIRA
A reimplementation/redesign of JIRA's board view

## Data
Board are uniquely identified and contain an array of tasks.
```
{
    board unique prefix<String>,
    id<Int>,
    name<String>,
    tasks<Array>: [
        Task Summary<Object>,
        Task Summary<Object>,
        Task Summary<Object>
    ]
}
```

A Task Summary is an object that keeps track of assignee, epic, reporter, status, ticket name, ticket description, time tracking, and any other descriptive fields.
```
{
    id<Int>,
    priority<Int>,
    task type<String>,
    title<String>,
    Assignee<Object>,
    estimate<String>,
    status<String>,
    description<String>,
    epic<Int>
}
```

An Assignee contains an id, name, and image.
```
{
    id<Int>,
    image<String>,
    name<String>
}
