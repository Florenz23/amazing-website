# GitHub API Functions Documentation

## File Operations

### Create or Update File
```js
create_or_update_file({
  owner: "username",
  repo: "repo-name",
  path: "path/to/file.txt",
  content: "file content",
  message: "commit message",
  branch: "main",
  sha: "existing-file-sha" // Optional, required for updates
})
```

### Push Multiple Files
```js
push_files({
  owner: "username",
  repo: "repo-name",
  branch: "main",
  files: [
    { path: "file1.txt", content: "content1" },
    { path: "file2.txt", content: "content2" }
  ],
  message: "commit message"
})
```

### Get File Contents
```js
get_file_contents({
  owner: "username",
  repo: "repo-name",
  path: "path/to/file.txt",
  branch: "main" // Optional
})
```

## Repository Operations

### Create Repository
```js
create_repository({
  name: "repo-name",
  description: "description", // Optional
  private: false,  // Optional
  autoInit: true   // Optional, initialize with README
})
```

### Search Repositories
```js
search_repositories({
  query: "search terms",
  page: 1,     // Optional
  perPage: 30  // Optional
})
```

### Fork Repository
```js
fork_repository({
  owner: "original-owner",
  repo: "repo-name",
  organization: "org-name" // Optional
})
```

### Create Branch
```js
create_branch({
  owner: "username",
  repo: "repo-name",
  branch: "new-branch",
  from_branch: "main" // Optional, defaults to default branch
})
```

## Issue and PR Management

### Create Issue
```js
create_issue({
  owner: "username",
  repo: "repo-name",
  title: "Issue title",
  body: "Issue description", // Optional
  assignees: ["user1"],      // Optional
  labels: ["bug"]            // Optional
})
```

### Create Pull Request
```js
create_pull_request({
  owner: "username",
  repo: "repo-name",
  title: "PR title",
  head: "feature-branch",
  base: "main",
  body: "PR description",     // Optional
  draft: false,               // Optional
  maintainer_can_modify: true // Optional
})