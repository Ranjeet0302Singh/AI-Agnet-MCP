# AI Agent

Hello! I am an AI Agent, and I'm here to assist you with various tasks on GitHub.

## What I can do:

*   **Repository Management**: I can create, fork, and manage repositories.
*   **Branch Operations**: I can create new branches, update existing files within branches, and manage pull requests.
*   **Issue and Pull Request Management**: I can create new issues and pull requests, add comments, list them, and get details about them.
*   **Code Review**: I can assist with code reviews by adding comments to pending reviews and submitting reviews.
*   **Workflow Automation**: I can list, get details, and manage workflow runs, including rerunning failed jobs or entire workflows.
*   **File Operations**: I can get file contents, create or update files, and delete files.
*   **Information Retrieval**: I can search for users, repositories, code, issues, pull requests, and organizations. I can also retrieve details about commits, releases, tags, discussions, and notifications.
*   **Collaboration**: I can add comments to issues and discussions, and manage team members and organizations.

I am continuously learning and improving to provide more comprehensive assistance for your GitHub workflows.

## My Capabilities (Tools I Can Use):

### Repository Management
*   `create_repository(name, autoInit, description, private)`: Create a new GitHub repository.
*   `fork_repository(owner, repo, organization)`: Fork a GitHub repository to your account or a specified organization.
*   `delete_file(branch, message, owner, path, repo)`: Delete a file from a GitHub repository.
*   `create_or_update_file(branch, content, message, owner, path, repo, sha)`: Create or update a single file in a GitHub repository.
*   `push_files(branch, files, message, owner, repo)`: Push multiple files to a GitHub repository in a single commit.
*   `get_file_contents(owner, repo, path, ref, sha)`: Get the contents of a file or directory from a GitHub repository.

### Branch Management
*   `create_branch(branch, owner, repo, from_branch)`: Create a new branch in a GitHub repository.
*   `list_branches(owner, repo, page, perPage)`: List branches in a GitHub repository.

### Pull Request Management
*   `create_pull_request(base, head, owner, repo, title, body, draft, maintainer_can_modify)`: Create a new pull request.
*   `list_pull_requests(owner, repo, base, direction, head, page, perPage, sort, state)`: List pull requests in a GitHub repository.
*   `get_pull_request(owner, pullNumber, repo)`: Get details of a specific pull request.
*   `get_pull_request_diff(owner, pullNumber, repo)`: Get the diff of a pull request.
*   `get_pull_request_files(owner, pullNumber, repo, page, perPage)`: Get the files changed in a specific pull request.
*   `update_pull_request(owner, pullNumber, repo, base, body, draft, maintainer_can_modify, reviewers, state, title)`: Update an existing pull request.
*   `merge_pull_request(owner, pullNumber, repo, commit_message, commit_title, merge_method)`: Merge a pull request.
*   `update_pull_request_branch(owner, pullNumber, repo, expectedHeadSha)`: Update the branch of a pull request with the latest changes from the base branch.

### Pull Request Reviews
*   `create_pending_pull_request_review(owner, pullNumber, repo, commitID)`: Create a pending review for a pull request.
*   `add_comment_to_pending_review(body, owner, path, pullNumber, repo, subjectType, line, side, startLine, startSide)`: Add a review comment to the requester's latest pending pull request review.
*   `submit_pending_pull_request_review(event, owner, pullNumber, repo, body)`: Submit the requester's latest pending pull request review.
*   `delete_pending_pull_request_review(owner, pullNumber, repo)`: Delete the requester's latest pending pull request review.
*   `create_and_submit_pull_request_review(body, event, owner, pullNumber, repo, commitID)`: Create and submit a review for a pull request without review comments.
*   `get_pull_request_reviews(owner, pullNumber, repo)`: Get reviews for a specific pull request.
*   `get_pull_request_comments(owner, pullNumber, repo)`: Get comments for a specific pull request.
*   `get_pull_request_status(owner, pullNumber, repo)`: Get the status of a specific pull request.

### Issue Management
*   `create_issue(owner, repo, title, assignees, body, labels, milestone, type)`: Create a new issue.
*   `list_issues(owner, repo, after, direction, labels, orderBy, perPage, since, state)`: List issues in a GitHub repository.
*   `get_issue(issue_number, owner, repo)`: Get details of a specific issue.
*   `update_issue(issue_number, owner, repo, assignees, body, labels, milestone, state, title, type)`: Update an existing issue.
*   `add_issue_comment(body, issue_number, owner, repo)`: Add a comment to a specific issue.
*   `get_issue_comments(issue_number, owner, repo, page, perPage)`: Get comments for a specific issue.
*   `list_issue_types(owner)`: List supported issue types for a repository owner (organization).
*   `add_sub_issue(issue_number, owner, repo, sub_issue_id, replace_parent)`: Add a sub-issue to a parent issue.
*   `list_sub_issues(issue_number, owner, repo, page, per_page)`: List sub-issues for a specific issue.
*   `remove_sub_issue(issue_number, owner, repo, sub_issue_id)`: Remove a sub-issue from a parent issue.
*   `reprioritize_sub_issue(issue_number, owner, repo, sub_issue_id, after_id, before_id)`: Reprioritize a sub-issue within a parent issue's sub-issue list.

### Code Scanning & Security
*   `list_code_scanning_alerts(owner, repo, ref, severity, state, tool_name)`: List code scanning alerts.
*   `get_code_scanning_alert(alertNumber, owner, repo)`: Get details of a specific code scanning alert.
*   `list_dependabot_alerts(owner, repo, severity, state)`: List Dependabot alerts.
*   `get_dependabot_alert(alertNumber, owner, repo)`: Get details of a specific Dependabot alert.
*   `list_secret_scanning_alerts(owner, repo, resolution, secret_type, state)`: List secret scanning alerts.
*   `get_secret_scanning_alert(alertNumber, owner, repo)`: Get details of a specific secret scanning alert.

### Gist Management
*   `create_gist(content, filename, description, public)`: Create a new gist.
*   `update_gist(content, filename, gist_id, description)`: Update an existing gist.
*   `list_gists(page, perPage, since, username)`: List gists for a user.

### Workflow and Actions
*   `list_workflows(owner, repo, page, perPage)`: List workflows in a repository.
*   `list_workflow_runs(owner, repo, workflow_id, actor, branch, event, page, perPage, status)`: List workflow runs for a specific workflow.
*   `get_workflow_run(owner, repo, run_id)`: Get details of a specific workflow run.
*   `list_workflow_jobs(owner, repo, run_id, filter, page, perPage)`: List jobs for a specific workflow run.
*   `get_job_logs(owner, repo, failed_only, job_id, return_content, run_id, tail_lines)`: Download logs for a specific workflow job or efficiently get all failed job logs for a workflow run.
*   `get_workflow_run_logs(owner, repo, run_id)`: Download logs for a specific workflow run (as a ZIP).
*   `list_workflow_run_artifacts(owner, repo, run_id, page, perPage)`: List artifacts for a workflow run.
*   `download_workflow_run_artifact(artifact_id, owner, repo)`: Get download URL for a workflow run artifact.
*   `cancel_workflow_run(owner, repo, run_id)`: Cancel a workflow run.
*   `rerun_workflow_run(owner, repo, run_id)`: Re-run an entire workflow run.
*   `rerun_failed_jobs(owner, repo, run_id)`: Re-run only the failed jobs in a workflow run.
*   `run_workflow(owner, ref, repo, workflow_id, inputs)`: Run an Actions workflow by workflow ID or filename.
*   `get_workflow_run_usage(owner, repo, run_id)`: Get usage metrics for a workflow run.
*   `delete_workflow_run_logs(owner, repo, run_id)`: Delete logs for a workflow run.

### Notifications
*   `list_notifications(before, filter, owner, page, perPage, repo, since)`: Lists all GitHub notifications for the authenticated user.
*   `get_notification_details(notificationID)`: Get detailed information for a specific GitHub notification.
*   `dismiss_notification(threadID, state)`: Dismiss a notification by marking it as read or done.
*   `manage_notification_subscription(action, notificationID)`: Manage a notification subscription (ignore, watch, or delete).
*   `manage_repository_notification_subscription(action, owner, repo)`: Manage a repository notification subscription.
*   `mark_all_notifications_read(lastReadAt, owner, repo)`: Mark all notifications as read.

### User and Teams
*   `get_me()`: Get details of the authenticated GitHub user.
*   `search_users(query, order, page, perPage, sort)`: Find GitHub users.
*   `search_orgs(query, order, page, perPage, sort)`: Find GitHub organizations.
*   `get_teams(user)`: Get details of the teams the user is a member of.
*   `get_team_members(org, team_slug)`: Get member usernames of a specific team in an organization.

### Discussions
*   `list_discussion_categories(owner, repo)`: List discussion categories.
*   `list_discussions(owner, after, category, direction, orderBy, perPage, repo)`: List discussions for a repository or organization.
*   `get_discussion(discussionNumber, owner, repo)`: Get a specific discussion by ID.
*   `get_discussion_comments(discussionNumber, owner, repo, after, perPage)`: Get comments from a discussion.

### Commits and Releases
*   `list_commits(owner, repo, author, page, perPage, sha)`: Get list of commits of a branch.
*   `get_commit(owner, repo, sha, page, perPage)`: Get details for a commit.
*   `list_tags(owner, repo, page, perPage)`: List git tags in a GitHub repository.
*   `get_tag(owner, repo, tag)`: Get details about a specific git tag.
*   `list_releases(owner, repo, page, perPage)`: List releases in a GitHub repository.
*   `get_latest_release(owner, repo)`: Get the latest release in a GitHub repository.

### GitHub Copilot Integration
*   `assign_copilot_to_issue(issueNumber, owner, repo)`: Assign Copilot to a specific issue.
*   `create_pull_request_with_copilot(owner, problem_statement, repo, title, base_ref)`: Delegate a task to GitHub Copilot coding agent to create a pull request with the implementation.
*   `request_copilot_review(owner, pullNumber, repo)`: Request a GitHub Copilot code review for a pull request.

### Search
*   `search_code(query, order, page, perPage, sort)`: Fast and precise code search across all GitHub repositories.
*   `search_issues(query, order, owner, page, perPage, repo, sort)`: Search for issues in GitHub repositories.
*   `search_pull_requests(query, order, owner, page, perPage, repo, sort)`: Search for pull requests in GitHub repositories.
*   `search_repositories(query, page, perPage)`: Find GitHub repositories.

### Internal Tool
*   `Think(input)`: Use this tool to think about something. It will not obtain new information or change the database, but just append the thought to the log. Use it when complex reasoning or some cache memory is needed.
