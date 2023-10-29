## Description

Issue: https://github.com/Software-Engineering-Red/MAUI-APP/issues/62
PR: https://github.com/Software-Engineering-Red/MAUI-APP/pull/90

The requirements for the issue is to be able to list partner agencies and their current association status. The list should also be filterable.

A new table containing partner agencies names and association statuses needs to be added, as well as a filtered list view.

```SQL
-- The query for the new table.
CREATE TABLE IF NOT EXISTS partner_agencies (Id INTEGER PRIMARY KEY AUTOINCREMENT, Name TEXT NOT NULL)
```

Due to how the project is currently structured the association status can not be added without a major rewrite, which I have touched upon in my PR comment, but this should be a good start on adding the functionality. As a plus, the way the code has been currently written does make it quite easy to add new tables.

## Reviews

No issues were found by the reviewer for the functionality I have added.

Reviewed issue: https://github.com/Software-Engineering-Red/MAUI-APP/pull/94
The issue I reviewed had a small problem that I quickly fixed to speed up the process, but everything worked as expected and best practices were followed.

## Reflection

- I got a little bit more familiar with the review process.
- Following a common workflow has really helped streamline the process of adding new functionality to the project.
- Not having a person in charge (like a project manager) does make it very hard to make core changes to the project.
- The team has discussed a rewrite so it is easier to add new functionality.
