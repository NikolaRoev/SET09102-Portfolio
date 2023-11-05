# Project work 2

## Description

Issue: https://github.com/Software-Engineering-Red/MAUI-APP/issues/63
PR: https://github.com/Software-Engineering-Red/MAUI-APP/pull/112

The issue I worked on for this week required adding a pool of experts to the application. The skill, location and status of each expert needed to be recorded, as well as the latest date and time of each expert's change in status.

Partial code of the model for the expert object used by the SQLite database.

```C#
public class Expert : INotifyPropertyChanged {
    [PrimaryKey, AutoIncrement]
    public int ID { get; set; }

    private string _skill;
    public string Skill {
        get => _skill;
        set => SetProperty(ref _skill, value);
    }

    private string _location;
    public string Location {
        get => _location;
        set => SetProperty(ref _location, value);
    }

    private string _status;
    public string Status {
        get => _status;
        set => SetStatus(value); 
    }

    private void SetStatus(string value) {
        SetProperty(ref _status, value);
        StatusChange = DateTime.Now.ToString();
    }

    public string StatusChange;

    ...
}
```

## Reviews

No issues were found by the reviewer for the functionality I have added.

Unfortunately I was not able to review an issue for this week as there were not a lot of tickets ready for review. This can be contributed to the rewrite, making it a little harder to add new code.

## Reflection

After an extensive restructuring of the application, the code needed for this week's issue was a lot more. Incorporating a new page in the application was now possible. There would still be a need for further restructuring so the different properties of each tracked object can more easily be displayed and edited, but this is certainly a good step in the right direction. Something we should maybe work on next is creating a test project for the application.

In the end the correctness of the project is not the primary goal, but the gain of experience in following best practices.