# Bug reporting

At BeyondATC, we do not use a formal ticketing system for bug tracking. Since our software is still in early access, many issues are general and may be resolved as development progresses. Instead, we rely on user-submitted bug reports to identify and address problems efficiently. Your reports are invaluable in helping us improve BeyondATC, but to be effective, **they must be clear, concise, and include all necessary details** to help the developers reproduce and fix the issue.

What does that mean?

- **We do not acknowledge every bug report individually**. 
- **We cannot always provide responses to every report**.
- **We cannot guarantee a timeframe for fixes**.

We truly appreciate everyone who takes the time to submit a bug report. We understand that not receiving direct feedback can be frustrating, but rest assured that all complete reports are reviewed. Reviewing and investigating bug reports requires time and effort, and prioritizing responses would take valuable resources away from fixing issues and developing new features.

## Where to report bugs
For bug reporting, please use our Discord channel *?!-batc-support*. Here, both our team and community members are available to assist with troubleshooting steps and provide guidance. When submitting a report, ensure that it is easy to understand and contains all relevant details. Following the structured approach below will increase the likelihood of your bug being identified and fixed promptly.

## How to write a bug report
A well-written bug report helps developers reproduce and fix the issue quickly. It should be complete but concise - overly long reports with unnecessary details are not necessary and can bring confusion.

Follow this checklist to make sure you are writing a good bug report:

- **Clearly describe the problem**. Report only one issue per bug report.
- **Provide context**. Explain what you were doing, where, and at what moment the issue occurred so developers can easily reproduce it.
- **State your expected outcome**. This ensures that what you were expecting aligns with the intended behavior.
- **Attach log files**. Log files are mandatory for <u>all bug reports</u> and provide essential details for debugging.
- **Include additional supporting materials if applicable**. Screenshots, Volanta flight tracking, charts, or video recordings can help clarify the issue.

!!! example "Examples of bug reports"

    === "❌ Bad example"

        > *I was flying, and the ATC told me to descend too fast. It doesn’t work correctly. Please fix it*

        Why is this bug report bad?

        - We have no context: where that happened? Which flight plan? 
        - What does it mean "too fast"? It's subjective, a precise number/data should be provided so we can define if it is too fast or not
        - No log file, no additional information that could help reproduce the issue
        - No need to ask to fix it, the purpose of a bug report is to identify and fix bugs :-)

    === "✅ Good example"

        > *LEBL, downwind leg of the LES2W transition, I received first vectoring instructions but no further vectors after that. Continued as instructed, ATC told me I was off course and gave me a direct to BL419. Here's the log file and flight tracking map.*

        Why is this bug report good?
        
        - We know the problem, the location, and which instruction was incorrect or missing 
        - The message is concise and complete
        - The log file is attached providing the full history of the flight
        - A flight tracking map can help understand where the issue happened

## Uploading log files
Log files are very important in helping us identify the root cause of the issue. Please upload your log files along with your bug report. The logs contain detailed information about BATC operations, such as errors that occurred during your session, flight plan used and the full history of your flight.

Navigate to the log files on your computer:  
```%userprofile%\appdata\locallow\Skirmish Mode Games, Inc\BeyondATC```

Find the following files in that directory:

- ```Player.log```: contains the log from your most recent flight. If the issue occurred during your last flight, please upload this log.
- ```Player-prev.log```: contains the log from the flight preceding your most recent one. If you completed another flight after encountering the issue, please send this log instead
- ```beyondATC.log```: This log provides insights into the BeyondATC application’s operations. If this file is not empty, please include it with your report.

Drag and drop these files directly into the Discord channel.

Mention your bug report when uploading the logs so that our team can correlate the log data with your specific issue.