git\_understanding



**Why are PRs important in a team workflow?**



&#x09;Pull requests(PR) are essentially a requests that needs approval, it contains documentations and changes a developer made in the codebase. It is done so that everyone in charge can review it first to check for bugs or possible errors before it is approved and made into production. It is very important as it ensures that teams are aware of changes in the codebase and possible issues are mitigated even before it is out there.



**What makes a well-structured PR?**



&#x09;A good PR has a brief explanation of what the PR does, What are the changes made, Why was that change used, and how to test the changes for review.



**What did you learn from reviewing an open source PR?**



&#x09;Reviewing an open source PR made me learn that PRs should be comprehensive and should include technical details that made the changes what it is. It also should include steps on how to test the change so that the reviewer can properly test it before approving for it.



**What makes a good commit message?**



&#x09;Good commit messages are usually short, specific, and action-oriented. It includes new features added, fixes made, refactors, documentation, style, test and maintenance.



**How does a clear commit message help in team collaboration?**

&#x09;

&#x09;It helps team understand what was the changes for and what to expect that changed by making certain commits. It also narrows the review and makes reviewing faster.



**How can poor commit messages issues later?**



&#x09;Poor commit messages such as vague messages, ambiguous, or lacks conclusive details can make debugging later on if it caused any issues. And that on its own can cost the organization money, time and effort just to figure out what went wrong.



**What does git bisect do?**



&#x09;Git bisect is a git tool used to find the exact commit that introduced a bug by doing a search that cuts the search space repeatedly until it identifies the problematic commit.



**When would you use it in a real-world debugging situation?**



&#x09;You would use it to find which commits or what changes lead to the issues you are currently experiencing. This would help you pinpoint what to fix and what to do to resolve the issue.



**How does it compare to manually reviewing commits?**

&#x09;

&#x09;Manually reviewing commits would take you more time just to identify a problem as supposed to using git bisect, you can find the problem faster and resolve the issue in a much earlier time.



**What does each command do?**



**git checkout main -- <file> :** helps you restore file from the main without affecting other changes.

**git cherry-pick <commit>** : This apply a specific commit from another branch without merging the whole branch.

**git log :** Shows you your commit history.

**git blame <file>** : See who last modified a line in the file and when was it modified.



**When would you use it in a real project?**



&#x09;This would typically be commonly used when your trying to resolve or fix an issue in the production and to pinpoint what caused it we will use this commands to check when, what, how, why and who might've caused it.



**What surprised you while testing these commands?**



&#x09;I'm surprised that you can actually see a lot more details about the commits. This makes things easier to debug and actually lessen time in debugging an issue.



**Why is pushing directly to main problematic?** 



&#x09;Pushing to the main is problematic because every change needs to be tested first as changes might carry unchecked conflicts or conflicts that is not accounted for. This conflicts might cause the production to fail and it would be a headache for the organization because the app will be essentially downed while the issue exists and the organization will lose money in return.



**How does branches help with reviewing code?** 


&#x09;Branches help in reviewing code because it is essentially a copy of the main branch so it is safer to test changes on a branch and you can review if everything is working before pushing it to production. 



**What happens if two people edit the same file on different branches?** 



&#x09;This will cause a conflict during the merging and it would require resolving before anyone push it to the main branch to be merged.





